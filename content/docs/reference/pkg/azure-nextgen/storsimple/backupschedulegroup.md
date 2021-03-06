
---
title: "BackupScheduleGroup"
title_tag: "azure-nextgen.storsimple.BackupScheduleGroup"
meta_desc: "Documentation for the azure-nextgen.storsimple.BackupScheduleGroup resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

The Backup Schedule Group
Latest API Version: 2016-10-01.

{{% examples %}}
## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}
### BackupScheduleGroupsCreateOrUpdate
{{% example csharp %}}
```csharp
using Pulumi;
using AzureNextGen = Pulumi.AzureNextGen;

class MyStack : Stack
{
    public MyStack()
    {
        var backupScheduleGroup = new AzureNextGen.StorSimple.Latest.BackupScheduleGroup("backupScheduleGroup", new AzureNextGen.StorSimple.Latest.BackupScheduleGroupArgs
        {
            DeviceName = "HSDK-4XY4FI2IVG",
            ManagerName = "hAzureSDKOperations",
            ResourceGroupName = "ResourceGroupForSDKTest",
            ScheduleGroupName = "BackupSchGroupForSDKTest",
            StartTime = ,
        });
    }

}

```

{{% /example %}}

{{% example go %}}

```go
package main

import (
	storsimple "github.com/pulumi/pulumi-azure-nextgen/sdk/go/azure/storsimple/latest"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := storsimple.NewBackupScheduleGroup(ctx, "backupScheduleGroup", &storsimple.BackupScheduleGroupArgs{
			DeviceName:        pulumi.String("HSDK-4XY4FI2IVG"),
			ManagerName:       pulumi.String("hAzureSDKOperations"),
			ResourceGroupName: pulumi.String("ResourceGroupForSDKTest"),
			ScheduleGroupName: pulumi.String("BackupSchGroupForSDKTest"),
			StartTime:         nil,
		})
		if err != nil {
			return err
		}
		return nil
	})
}

```

{{% /example %}}

{{% example python %}}

```python
import pulumi
import pulumi_azure_nextgen as azure_nextgen

backup_schedule_group = azure_nextgen.storsimple.latest.BackupScheduleGroup("backupScheduleGroup",
    device_name="HSDK-4XY4FI2IVG",
    manager_name="hAzureSDKOperations",
    resource_group_name="ResourceGroupForSDKTest",
    schedule_group_name="BackupSchGroupForSDKTest",
    start_time=azure_nextgen.storsimple.latest.TimeArgs())

```

{{% /example %}}

{{% example typescript %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_nextgen from "@pulumi/azure-nextgen";

const backupScheduleGroup = new azure_nextgen.storsimple.latest.BackupScheduleGroup("backupScheduleGroup", {
    deviceName: "HSDK-4XY4FI2IVG",
    managerName: "hAzureSDKOperations",
    resourceGroupName: "ResourceGroupForSDKTest",
    scheduleGroupName: "BackupSchGroupForSDKTest",
    startTime: {},
});

```

{{% /example %}}

{{% /examples %}}


## Create a BackupScheduleGroup Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">BackupScheduleGroup</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p">:</span> <span class="nx">BackupScheduleGroupArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nx">BackupScheduleGroup</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">device_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">manager_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">schedule_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">start_time</span><span class="p">:</span> <span class="nx">Optional[TimeArgs]</span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewBackupScheduleGroup</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">, </span><span class="nx">args</span><span class="p"> </span><span class="nx">BackupScheduleGroupArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">BackupScheduleGroup</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">BackupScheduleGroup</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx">BackupScheduleGroupArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
  
    <dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type">BackupScheduleGroupArgs</span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd>
  
    <dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd>
  

</dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">
            <a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a>
        </span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
  
    <dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>
      Context object for the current deployment.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type">BackupScheduleGroupArgs</span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd>
  
    <dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd>
  

</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
  
    <dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type">BackupScheduleGroupArgs</span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd>
  
    <dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd>
  

</dl>

{{% /choosable %}}

## BackupScheduleGroup Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/programming-model#outputs" >}}) in the Programming Model docs.

### Inputs

The BackupScheduleGroup resource accepts the following [input]({{< relref "/docs/intro/concepts/programming-model#outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="devicename_csharp">
<a href="#devicename_csharp" style="color: inherit; text-decoration: inherit;">Device<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the device.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="managername_csharp">
<a href="#managername_csharp" style="color: inherit; text-decoration: inherit;">Manager<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The manager name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource group name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="schedulegroupname_csharp">
<a href="#schedulegroupname_csharp" style="color: inherit; text-decoration: inherit;">Schedule<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the schedule group.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="starttime_csharp">
<a href="#starttime_csharp" style="color: inherit; text-decoration: inherit;">Start<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#time">Pulumi.<wbr>Azure<wbr>Next<wbr>Gen.<wbr>Stor<wbr>Simple.<wbr>Inputs.<wbr>Time<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The start time. When this field is specified we will generate Default GrandFather Father Son Backup Schedules.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="devicename_go">
<a href="#devicename_go" style="color: inherit; text-decoration: inherit;">Device<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the device.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="managername_go">
<a href="#managername_go" style="color: inherit; text-decoration: inherit;">Manager<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The manager name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource group name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="schedulegroupname_go">
<a href="#schedulegroupname_go" style="color: inherit; text-decoration: inherit;">Schedule<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the schedule group.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="starttime_go">
<a href="#starttime_go" style="color: inherit; text-decoration: inherit;">Start<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#time">Time</a></span>
    </dt>
    <dd>{{% md %}}The start time. When this field is specified we will generate Default GrandFather Father Son Backup Schedules.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="devicename_nodejs">
<a href="#devicename_nodejs" style="color: inherit; text-decoration: inherit;">device<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the device.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="managername_nodejs">
<a href="#managername_nodejs" style="color: inherit; text-decoration: inherit;">manager<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The manager name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource group name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="schedulegroupname_nodejs">
<a href="#schedulegroupname_nodejs" style="color: inherit; text-decoration: inherit;">schedule<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the schedule group.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="starttime_nodejs">
<a href="#starttime_nodejs" style="color: inherit; text-decoration: inherit;">start<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#time">Time</a></span>
    </dt>
    <dd>{{% md %}}The start time. When this field is specified we will generate Default GrandFather Father Son Backup Schedules.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="device_name_python">
<a href="#device_name_python" style="color: inherit; text-decoration: inherit;">device_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the device.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="manager_name_python">
<a href="#manager_name_python" style="color: inherit; text-decoration: inherit;">manager_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The manager name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource group name{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="schedule_group_name_python">
<a href="#schedule_group_name_python" style="color: inherit; text-decoration: inherit;">schedule_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the schedule group.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="start_time_python">
<a href="#start_time_python" style="color: inherit; text-decoration: inherit;">start_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#time">Time<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The start time. When this field is specified we will generate Default GrandFather Father Son Backup Schedules.{{% /md %}}</dd>
</dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the BackupScheduleGroup resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name.{{% /md %}}</dd>
    <dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type.{{% /md %}}</dd>
</dl>
{{% /choosable %}}







## Supporting Types



<h4 id="time">Time</h4>

{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_csharp">
<a href="#hours_csharp" style="color: inherit; text-decoration: inherit;">Hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_csharp">
<a href="#minutes_csharp" style="color: inherit; text-decoration: inherit;">Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_csharp">
<a href="#seconds_csharp" style="color: inherit; text-decoration: inherit;">Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_go">
<a href="#hours_go" style="color: inherit; text-decoration: inherit;">Hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_go">
<a href="#minutes_go" style="color: inherit; text-decoration: inherit;">Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_go">
<a href="#seconds_go" style="color: inherit; text-decoration: inherit;">Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_nodejs">
<a href="#hours_nodejs" style="color: inherit; text-decoration: inherit;">hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_nodejs">
<a href="#minutes_nodejs" style="color: inherit; text-decoration: inherit;">minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_nodejs">
<a href="#seconds_nodejs" style="color: inherit; text-decoration: inherit;">seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_python">
<a href="#hours_python" style="color: inherit; text-decoration: inherit;">hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_python">
<a href="#minutes_python" style="color: inherit; text-decoration: inherit;">minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_python">
<a href="#seconds_python" style="color: inherit; text-decoration: inherit;">seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

<h4 id="timeresponse">Time<wbr>Response</h4>

{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_csharp">
<a href="#hours_csharp" style="color: inherit; text-decoration: inherit;">Hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_csharp">
<a href="#minutes_csharp" style="color: inherit; text-decoration: inherit;">Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_csharp">
<a href="#seconds_csharp" style="color: inherit; text-decoration: inherit;">Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_go">
<a href="#hours_go" style="color: inherit; text-decoration: inherit;">Hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_go">
<a href="#minutes_go" style="color: inherit; text-decoration: inherit;">Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_go">
<a href="#seconds_go" style="color: inherit; text-decoration: inherit;">Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_nodejs">
<a href="#hours_nodejs" style="color: inherit; text-decoration: inherit;">hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_nodejs">
<a href="#minutes_nodejs" style="color: inherit; text-decoration: inherit;">minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_nodejs">
<a href="#seconds_nodejs" style="color: inherit; text-decoration: inherit;">seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="hours_python">
<a href="#hours_python" style="color: inherit; text-decoration: inherit;">hours</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The hour.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="minutes_python">
<a href="#minutes_python" style="color: inherit; text-decoration: inherit;">minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minute.{{% /md %}}</dd>
    <dt class="property-required"
            title="Required">
        <span id="seconds_python">
<a href="#seconds_python" style="color: inherit; text-decoration: inherit;">seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The second.{{% /md %}}</dd>
</dl>
{{% /choosable %}}
## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-nextgen:storsimple/latest:BackupScheduleGroup BackupSchGroupForSDKTest /subscriptions/9eb689cd-7243-43b4-b6f6-5c65cb296641/resourceGroups/ResourceGroupForSDKTest/providers/Microsoft.StorSimple/managers/hAzureSDKOperations/devices/hsdk-4xy4fi2ivg/backupScheduleGroups/BackupSchGroupForSDKTest 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-nextgen">https://github.com/pulumi/pulumi-azure-nextgen</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

