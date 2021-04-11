---
description: 除了透過 [元件服務] 系統管理工具來建立和設定本機資料分割之外，您還可以使用資料分割專屬的 COM + 系統管理集合和屬性，以程式設計方式管理分割區。
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: 管理本機磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936475"
---
# <a name="managing-local-partitions"></a><span data-ttu-id="55986-103">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="55986-103">Managing Local Partitions</span></span>

<span data-ttu-id="55986-104">除了透過 [元件服務] 系統管理工具來建立和設定本機資料分割之外，您還可以使用資料分割專屬的 COM + 系統管理集合和屬性，以程式設計方式管理分割區。</span><span class="sxs-lookup"><span data-stu-id="55986-104">As an alternative to creating and configuring local partitions through the Component Services administrative tool, you can manage partitions programmatically by using partition-specific COM+ administration collections and properties.</span></span>

> [!Note]  
> <span data-ttu-id="55986-105">預設不會啟用 COM + 分割服務。</span><span class="sxs-lookup"><span data-stu-id="55986-105">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="55986-106">若要使用 COM + 分割服務，您必須透過 [元件服務] 系統管理工具啟用它，或將 [**LocalComputer**](localcomputer.md) 集合上的 PartitionsEnabled 屬性變更為 True。</span><span class="sxs-lookup"><span data-stu-id="55986-106">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="55986-107">下列以 Visual Basic 腳本撰寫的副程式示範如何在本機電腦上建立磁碟分割：</span><span class="sxs-lookup"><span data-stu-id="55986-107">The following subroutine written in Visual Basic script demonstrates how to create a partition on the local computer:</span></span>


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



<span data-ttu-id="55986-108">下列以 Visual Basic 腳本撰寫的副程式示範如何從本機電腦刪除分割區：</span><span class="sxs-lookup"><span data-stu-id="55986-108">The following subroutine written in Visual Basic script demonstrates how to delete a partition from the local computer:</span></span>


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="55986-109">下列以 Visual Basic 腳本撰寫的副程式示範如何設定使用者的預設分割區：</span><span class="sxs-lookup"><span data-stu-id="55986-109">The following subroutine written in Visual Basic script demonstrates how to set the default partition for a user:</span></span>


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="55986-110">下列以 Visual Basic 腳本撰寫的副程式會示範如何移除使用者的預設分割區：</span><span class="sxs-lookup"><span data-stu-id="55986-110">The following subroutine written in Visual Basic script demonstrates how to remove the default partition for a user:</span></span>


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="55986-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="55986-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55986-112">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="55986-112">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="55986-113">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="55986-113">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="55986-114">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="55986-114">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="55986-115">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="55986-115">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="55986-116">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="55986-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



