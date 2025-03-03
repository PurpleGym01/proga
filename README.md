# 1. ������������� Git-����������� (���� ��� �� ���������������)
git init

# 2. ���������� ���� ������ � ����������� � ������ ������
git add .
git commit -m "Initial commit: CMake project setup"

# 3. �������� ����� ����� featureutils
git branch featureutils
git checkout featureutils  # ������������� �� ����� �����

# 4. �������� ��������� � utils.cpp (���������� ������� ���������)
#    � ���������� main.cpp ��� ������������� ���� �������
# (����������� �����, ����� ��������� � �������� ���������)

git add utils.cpp main.cpp
git commit -m "feat: Add multiplication function to utils"

# 5. ������������ ������� �� �������� ����� (main ��� master)
git checkout main  # ���� �������� ����� ���������� master, �������� main �� master

# 6. �������� ��������� � main.cpp � ������
git add main.cpp
git commit -m "fix: Update main output message in main branch"

# 7. ������� ����� ����� featureutils � ��������
git merge featureutils

# 8. ���������� ���������� (���� ��������)
# (��������� �����, ��������� ���������, ����� ����������)

git add .
git commit -m "merge: Resolve conflicts between main and featureutils"

# 9. �������� ���� ����� � ��������� �����������
git push --all origin
