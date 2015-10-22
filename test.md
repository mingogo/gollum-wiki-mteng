This is a regular paragraph. 

	register(DeltaBuilder.update("2.5", "")
	            .addTask(new NodeExistsDelegateTask("stkBlogEntryHeader dialog migration", "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/date",
	                    new ArrayDelegateTask("stkBlogEntryHeader dialog migration", "Migration of date field",
	                            new RemovePropertyTask("", "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/date", "value"),
	                            new RemovePropertyTask("", "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/date", "controlType"),
	                            new SetPropertyTask(RepositoryConstants.CONFIG, "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/date", "class", "info.magnolia.ui.form.field.definition.DateFieldDefinition")
	            )))
	            .addTask(new NodeExistsDelegateTask("stkBlogEntryHeader dialog migration", "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/author",
	                    new ArrayDelegateTask("stkBlogEntryHeader dialog migration", "Migration of author field",
	                            new RemovePropertyTask("", "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/author", "value"),
	                            new RemovePropertyTask("", "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/author", "controlType"),
	                            new SetPropertyTask(RepositoryConstants.CONFIG, "/modules/standard-templating-kit/dialogs/pages/blogEntry/stkBlogEntryHeader/form/tabs/tabMain/fields/author", "class", "info.magnolia.ui.form.field.definition.TextFieldDefinition")
	            )))
	            .addTask(new NodeExistsDelegateTask("Removing obsolete blog controls", "/modules/blog/controls",
	                    new RemoveNodeTask("Removing obsolete blog controls", "/modules/blog/controls")
	            ))
	         );
