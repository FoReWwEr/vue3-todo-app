<template>
  <div class="todoapp">
      <h1 class="todoapp__title">todos</h1>

      <div class="todoapp__content">
        <header class="todoapp__header">
          <button
            type="button"
            class="todoapp__toggle-all active"
            data-cy="ToggleAllButton"
          />

          <form>
            <input
              data-cy="NewTodoField"
              type="text"
              class="todoapp__new-todo"
              placeholder="What needs to be done?"
            />
          </form>
        </header>

        <section class="todoapp__main" data-cy="TodoList">
          <div data-cy="Todo" class="todo completed">
            <label class="todo__status-label">
              <input
                data-cy="TodoStatus"
                type="checkbox"
                class="todo__status"
                checked
              />
            </label>

            <span data-cy="TodoTitle" class="todo__title">
              Completed Todo
            </span>

            <button type="button" class="todo__remove" data-cy="TodoDelete">
              ×
            </button>

            <div data-cy="TodoLoader" class="modal overlay">
              <div class="modal-background has-background-white-ter" />
              <div class="loader" />
            </div>
          </div>

          <div data-cy="Todo" class="todo">
            <label class="todo__status-label">
              <input
                data-cy="TodoStatus"
                type="checkbox"
                class="todo__status"
              />
            </label>

            <span data-cy="TodoTitle" class="todo__title">
              Not Completed Todo
            </span>
            <button type="button" class="todo__remove" data-cy="TodoDelete">
              ×
            </button>

            <div data-cy="TodoLoader" class="modal overlay">
              <div class="modal-background has-background-white-ter" />
              <div class="loader" />
            </div>
          </div>

          <div data-cy="Todo" class="todo">
            <label class="todo__status-label">
              <input
                data-cy="TodoStatus"
                type="checkbox"
                class="todo__status"
              />
            </label>

            <form>
              <input
                data-cy="TodoTitleField"
                type="text"
                class="todo__title-field"
                placeholder="Empty todo will be deleted"
                value="Todo is being edited now"
              />
            </form>

            <div data-cy="TodoLoader" class="modal overlay">
              <div class="modal-background has-background-white-ter" />
              <div class="loader" />
            </div>
          </div>

          <div data-cy="Todo" class="todo">
            <label class="todo__status-label">
              <input
                data-cy="TodoStatus"
                type="checkbox"
                class="todo__status"
              />
            </label>

            <span data-cy="TodoTitle" class="todo__title">
              Todo is being saved now
            </span>

            <button type="button" class="todo__remove" data-cy="TodoDelete">
              ×
            </button>

            <div data-cy="TodoLoader" class="modal overlay is-active">
              <div class="modal-background has-background-white-ter" />
              <div class="loader" />
            </div>
          </div>
        </section>

        <footer class="todoapp__footer" data-cy="Footer">
          <span class="todo-count" data-cy="TodosCounter">
            3 items left
          </span>

          <nav class="filter" data-cy="Filter">
            <a
              href="#/"
              class="filter__link selected"
              data-cy="FilterLinkAll"
            >
              All
            </a>

            <a
              href="#/active"
              class="filter__link"
              data-cy="FilterLinkActive"
            >
              Active
            </a>

            <a
              href="#/completed"
              class="filter__link"
              data-cy="FilterLinkCompleted"
            >
              Completed
            </a>
          </nav>

          <button
            type="button"
            class="todoapp__clear-completed"
            data-cy="ClearCompletedButton"
          >
            Clear completed
          </button>
        </footer>
      </div>

      <div
        data-cy="ErrorNotification"
        class="notification is-danger is-light has-text-weight-normal"
      >
        <button data-cy="HideErrorButton" type="button" class="delete" />
        Unable to load todos
        <br />
        Title should not be empty
        <br />
        Unable to add a todo
        <br />
        Unable to delete a todo
        <br />
        Unable to update a todo
      </div>
    </div>
</template>
