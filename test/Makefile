all:
	@echo "Try make check"

check:
	psql -f ../pyramid.sql
	psql -XtA -v "VERBOSITY=terse" < cdb_torquepixel_add_test.sql 2>&1 | diff -U2 cdb_torquepixel_add_test_expected -
	psql -XtA -v "VERBOSITY=terse" < cdb_torquepixel_del_test.sql 2>&1 | diff -U2 cdb_torquepixel_del_test_expected -
	psql -XtA -v "VERBOSITY=terse" < cdb_torquepixel_agg_test.sql 2>&1 | diff -U2 cdb_torquepixel_agg_test_expected -
	psql -XtA -v "VERBOSITY=terse" < cdb_torquepixel_dump_test.sql 2>&1 | diff -U2 cdb_torquepixel_dump_test_expected -
	psql -XtA -v "VERBOSITY=terse" < cdb_torquepixel_sum_test.sql 2>&1 | diff -U2 cdb_torquepixel_sum_test_expected -
	psql -XtA -v "VERBOSITY=terse" < cdb_pyramid_trigger_test.sql 2>&1 | diff -U2 cdb_pyramid_trigger_test_expected -

