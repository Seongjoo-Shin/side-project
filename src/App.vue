<template>
    <b-table
        :items="items"
        :fields="fields"
        :sort-by="sortBy"
        :sort-desc="sortDesc"
        @sort-changed="onSortChanged"
        caption="게시판"
    >
        <template #cell(actions)="row">
            <b-button
                size="sm"
                variant="primary"
                class="mr-1"
                @click="editItem(row.item)"
            >
                수정
            </b-button>
            <b-button size="sm" variant="danger" @click="deleteItem(row.item)">
                삭제
            </b-button>
        </template>
    </b-table>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    id: 1,
                    title: '첫 번째 게시물',
                    author: '홍길동',
                    created_at: '2022-02-01',
                    views: 100,
                    likes: 50,
                },
                {
                    id: 2,
                    title: '두 번째 게시물',
                    author: '김철수',
                    created_at: '2022-02-02',
                    views: 200,
                    likes: 100,
                },
                {
                    id: 3,
                    title: '세 번째 게시물',
                    author: '이영희',
                    created_at: '2022-02-03',
                    views: 300,
                    likes: 150,
                },
            ],
            fields: [
                { key: 'id', label: '번호', sortable: true },
                { key: 'title', label: '제목', sortable: true },
                { key: 'author', label: '작성자', sortable: true },
                { key: 'created_at', label: '작성일', sortable: true },
                { key: 'views', label: '조회수', sortable: true },
                { key: 'likes', label: '좋아요', sortable: true },
                { key: 'actions', label: '작업' },
            ],
            sortBy: 'id',
            sortDesc: false,
        };
    },
    methods: {
        onSortChanged(sortInfo) {
            this.sortBy = sortInfo.field;
            this.sortDesc = sortInfo.order === 'desc';
        },
        editItem(item) {
            // TODO: 게시물 수정 기능 구현
        },
        deleteItem(item) {
            // TODO: 게시물 삭제 기능 구현
        },
    },
};
</script>
