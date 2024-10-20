---
title: Access Apache Airflow Job Logs
description: This article explains how to access Apache Airflow Job logs through Apache Airflow Job UI.
ms.reviewer: xupxhou
ms.author: abnarain
author: abnarain
ms.topic: how-to
ms.date: 10/10/2024
---

# Access Apache Airflow Job Logs

> [!NOTE]
> Apache Airflow Job is powered by Apache Airflow.</br>[Apache Airflow](https://airflow.apache.org/) is an open-source platform used to programmatically create, schedule, and monitor complex jobs. It allows you to define a set of tasks, called operators, that can be combined into directed acyclic graphs (DAGs) to represent data pipelines.

This article shows you how to access Apache Airflow job logs through the Apache Airflow Job UI. 

## Prerequisites

To get started, you must complete the following prerequisites:

- Enable Apache Airflow Job in your Tenant.

  > [!NOTE]
  > Since Apache Airflow job is in preview state, you need to enable it through your tenant admin. If you already see Apache Airflow Job, your tenant admin may have already enabled it.

  1. Go to Admin Portal -> Tenant Settings -> Under Microsoft Fabric -> Expand "Users can create and use Apache Airflow Job (preview)" section.

  2. Select Apply.
     :::image type="content" source="media/apache-airflow-jobs/enable-apache-airflow-job-tenant.png" lightbox="media/apache-airflow-jobs/enable-apache-airflow-job-tenant.png" alt-text="Screenshot to enable Apache Airflow in tenant.":::

- Create or use an existing workspace in Microsoft Fabric.

- [Create or use an existing Apache Airflow job in Microsoft Fabric.](../data-factory/create-apache-airflow-jobs.md)

### Create and Run the Apache Airflow Job

We use default Directed Acyclic Graph (DAG), which is automatically created when a new file is added to Dags folder of Fabric managed storage.

1. Create a new file in Dags folder. A Dag is initialized consisting of BashOperator that prints "Hello world" in Apache Airflow Job logs.

   :::image type="content" source="media/apache-airflow-jobs/create-new-file.png" lightbox="media/apache-airflow-jobs/create-new-file.png" alt-text="Screenshot to create a new Apache Airflow file.":::

2. Save and Run the DAG within the Apache Airflow UI.

   :::image type="content" source="media/apache-airflow-jobs/save-and-run-dag.png" lightbox="media/apache-airflow-jobs/save-and-run-dag.png" alt-text="Screenshot to save and run the Apache Airflow Dag.":::

### Access logs of Apache Airflow Job

1. When the DAG runs, its logs are displayed in the results section. Click on Arrow, to expand the results section.
   :::image type="content" source="media/apache-airflow-jobs/access-result-section.png" lightbox="media/apache-airflow-jobs/access-result-section.png" alt-text="Screenshot to access the results section in Apache Airflow job.":::

2. Click on "Cluster logs" tab to access logs.
   :::image type="content" source="media/apache-airflow-jobs/cluster-tab.png" lightbox="media/apache-airflow-jobs/cluster-tab.png" alt-text="Screenshot to click on cluster logs.":::

3. Apply filters to choose the `Start time` and `Log type` of the logs.
   :::image type="content" source="media/apache-airflow-jobs/apply-filters.png" lightbox="media/apache-airflow-jobs/apply-filters.png" alt-text="Screenshot to apply filters on cluster logs.":::

4. Access the logs.
   :::image type="content" source="media/apache-airflow-jobs/apache-airflow-job-logs.png" lightbox="media/apache-airflow-jobs/apache-airflow-job-logs.png" alt-text="Screenshot to see cluster logs.":::


## Related Content

[Quickstart: Create an Apache Airflow Job](../data-factory/create-apache-airflow-jobs.md)