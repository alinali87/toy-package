poetry install  # install venv with deps
poetry shell  # activate venv
exit  # exit venv

poetry add <package_name>  # install a package, poetry will add it into dependencies automatically
poetry remove <package_name>  # uninstall a package, poetry will remove it from deps
poetry add --group dev <package_name>  # install a package into the dev group
poetry remove --group dev <package_name>  # uninstall a package from the dev group

poetry update  # update all deps according to specified versions
poetry update <package_name>  # update a specific package

poetry update --lock  # update only lock file

poetry build  # build the package

poetry run python -m pip install .  # install current directory as a package
pip install .  # this shorter version is available when venv is activated, NB. shorter version also works for the next commands
poetry run python -m pip install dist/<wheel_file_name>  # install from wheel-file
poetry run python -m pip install git+https://github.com/<account_name>/<repo_name>.git