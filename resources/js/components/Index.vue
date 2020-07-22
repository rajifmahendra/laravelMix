<template>
    <div class="card">
        <div class="card-header">
            <router-link to="/create" class="btn btn-primary">Tambah Buku</router-link>
        </div>

        <div class="card-body">
            <table class="table table-hover">
                <thead>
                    <tr>
                    <th scope="col">Title</th>
                    <th scope="col">Deskripsi</th>
                    <th width="100"></th>
                    <th width="100"></th>
                    <th width="100"></th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>masukkan title</td>
                        <td>masukkan deskripsi</td>
                        <td><button class="btn btn-info">Lihat</button></td>
                        <td><button class="btn btn-success">Edit</button></td>
                        <td><button class="btn btn-danger">Hapus</button></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>