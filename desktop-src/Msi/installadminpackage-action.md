---
description: InstallAdminPackage 動作會將產品資料庫複製到 TARGETDIR 屬性所定義的系統管理安裝點。
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: InstallAdminPackage 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943992"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="10149-103">InstallAdminPackage 動作</span><span class="sxs-lookup"><span data-stu-id="10149-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="10149-104">InstallAdminPackage 動作會將產品資料庫複製到 [**TARGETDIR**](targetdir.md) 屬性所定義的系統管理安裝點。</span><span class="sxs-lookup"><span data-stu-id="10149-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="10149-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="10149-105">Sequence Restrictions</span></span>

<span data-ttu-id="10149-106">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="10149-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="10149-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="10149-107">ActionData Messages</span></span>



| <span data-ttu-id="10149-108">欄位</span><span class="sxs-lookup"><span data-stu-id="10149-108">Field</span></span> | <span data-ttu-id="10149-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="10149-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="10149-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="10149-110">\[1\]</span></span> | <span data-ttu-id="10149-111">安裝檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="10149-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="10149-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="10149-112">\[6\]</span></span> | <span data-ttu-id="10149-113">資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="10149-113">Size of database.</span></span>                                          |
| <span data-ttu-id="10149-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="10149-114">\[9\]</span></span> | <span data-ttu-id="10149-115">系統管理安裝–點目錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10149-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="10149-116">備註</span><span class="sxs-lookup"><span data-stu-id="10149-116">Remarks</span></span>

<span data-ttu-id="10149-117">InstallAdminPackage 動作也會更新資料庫的摘要資訊，並在複製資料庫之後，移除任何位於資料流程中的封包檔。</span><span class="sxs-lookup"><span data-stu-id="10149-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



