#__Alex Lagutenko__
#__Junior Frontend Developer__
#__Contact:__
*__Phone__: +8 965 999 99 99
*__E-mail__: laxelaalexla@gmail.com

#__About Myself__:
*I want to learn Front-End Development in RSSchool!

#__Work experience__:
*Java
*Maven
*Spring
*Spring Boot
*Spting Data

#__Code__:
```
public class AppController {
    private Service employeeService;
    private Mapper employeeMapper;

    @RequestMapping(path = "/test", method = RequestMethod.GET)
    public String test() {
        return "Ура, работает!";
    }

    @PostMapping(path = "/add")
    public void createEmployee(@RequestBody EmployeeDtoRq employeeDtoRq) {
        log.info(employeeDtoRq.toString());
        employeeService.addEmployee(employeeMapper.convertEmployeeRq(employeeDtoRq));
    }
    @PostMapping(path = "/del/{id}")
    public void deleteEmployee(@PathVariable Integer id) {
        employeeService.deleteEmployee(id);
    }

    @GetMapping(path = "/get/{id}")
    public String getEmployeeId(@PathVariable Integer id) {

        return employeeService.getEmployeeId(id);
    }

    @PostMapping(path = "/update/{id}")
    public void updateEmployee(@PathVariable Integer id, @RequestBody EmployeeDtoRq employeeDtoRq) {

        employeeService.updateEmployee(id, employeeMapper.convertEmployeeRq(employeeDtoRq));
    }

    @GetMapping(path = "/log")
    public String getLog() {
       return employeeService.toString();
    }
}

[https://github.com/XeLaLA/homework2Modul5.git](адрес "GitHub")

#__Language__:

