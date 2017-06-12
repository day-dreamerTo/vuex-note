<template>
    <div id="toolbar">
        <i @click="addNote" class="glyphicon glyphicon-plus"></i>
        <i @click="toggleFavorite" class="glyphicon glyphicon-star" :class="{starred: activeNote && activeNote.favorite}"></i>
        <i @click="deleteNote" class="glyphicon glyphicon-remove"></i>
    </div>
</template>
<script type="text/ecmascript-6">
    import {addNote, deleteNote, toggleFavorite} from '../vuex/actions';
    export default{
        vuex: {
            getters: {
                activeNote: state => {
                    return state.activeNote;
                }
            },
            actions: {
                addNote, deleteNote, toggleFavorite
            }
        }
    };
</script>