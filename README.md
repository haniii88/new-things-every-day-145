/* New Things Every Day — Day 145 */
/* Analyzes project issues and creates an issue tracking report */

function dailyLog145() {
    const issues = [
        { id: 101, priority: "High", status: "Open" },
        { id: 102, priority: "Medium", status: "Closed" },
        { id: 103, priority: "Low", status: "Open" },
        { id: 104, priority: "High", status: "Closed" },
        { id: 105, priority: "Medium", status: "Open" }
    ];

    const openIssues = issues.filter(
        issue => issue.status === "Open"
    );

    const highPriority = issues.filter(
        issue => issue.priority === "High"
    );

    const report = {
        day: 145,
        timestamp: new Date().toISOString(),
        totalIssues: issues.length,
        openIssues: openIssues.length,
        closedIssues: issues.length - openIssues.length,
        highPriorityIssues: highPriority.length,
        status: "Issue tracking report generated successfully."
    };

    console.log("Day 145 Issue Report:", report);
}

dailyLog145();
