---
title: 建立和執行視圖
description: 您可以建立從 Active Directory 取得的資料檢視。 請注意，只有 view 定義會儲存在 SQL Server 中，而不是儲存在實際的結果集。 因此，當您稍後叫用 view 時，可能會得到不同的結果。
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371845"
---
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="6ad3b-105">建立和執行視圖</span><span class="sxs-lookup"><span data-stu-id="6ad3b-105">Creating and Executing a View</span></span>

<span data-ttu-id="6ad3b-106">您可以建立從 Active Directory 取得的資料檢視。</span><span class="sxs-lookup"><span data-stu-id="6ad3b-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="6ad3b-107">請注意，只有 view 定義會儲存在 SQL Server 中，而不是儲存在實際的結果集。</span><span class="sxs-lookup"><span data-stu-id="6ad3b-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="6ad3b-108">因此，當您稍後叫用 view 時，可能會得到不同的結果。</span><span class="sxs-lookup"><span data-stu-id="6ad3b-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="6ad3b-109">下列程式碼範例示範如何建立視圖。</span><span class="sxs-lookup"><span data-stu-id="6ad3b-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="6ad3b-110">使用下列程式碼來叫用 view。</span><span class="sxs-lookup"><span data-stu-id="6ad3b-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="6ad3b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ad3b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ad3b-112">在 SQL Server 和 Active Directory 之間建立異類聯結</span><span class="sxs-lookup"><span data-stu-id="6ad3b-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




