def calculate_sum_of_squares(y_values):
    sum_squares = 0
    for y in y_values:
        if -100 <= y <= 100:
            sum_squares += y ** 2
    return sum_squares

def main():
    # Read the number of test cases
    num_test_cases = int(input())
    assert 1 <= num_test_cases <= 100, "Number of test cases should be between 1 and 100"

    results = []


    for _ in range(num_test_cases):
        x = int(input())
        assert 0 < x <= 100, "X should be between 1 and 100"

        y_values = list(map(int, input().split()))
        assert len(y_values) == x, "Number of Yn values should match X"

        result = calculate_sum_of_squares(y_values)
        results.append(result)

    for result in results:
        print(result)


if _name_ == "_main_":
    main()
