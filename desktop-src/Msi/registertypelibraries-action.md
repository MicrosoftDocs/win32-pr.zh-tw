---
description: RegisterTypeLibraries 動作會向系統註冊類型程式庫。 此動作會套用至已排程要安裝之 TypeLib 資料表中所參考的每個檔案。
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: RegisterTypeLibraries 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977309"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="cc2cb-104">RegisterTypeLibraries 動作</span><span class="sxs-lookup"><span data-stu-id="cc2cb-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="cc2cb-105">RegisterTypeLibraries 動作會向系統註冊類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="cc2cb-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="cc2cb-106">此動作會套用至已排程要安裝之 [TypeLib 資料表](typelib-table.md) 中所參考的每個檔案。</span><span class="sxs-lookup"><span data-stu-id="cc2cb-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cc2cb-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="cc2cb-107">Sequence Restrictions</span></span>

<span data-ttu-id="cc2cb-108">RegisterTypeLibraries 動作必須晚于 [InstallFiles](installfiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="cc2cb-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cc2cb-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="cc2cb-109">ActionData Messages</span></span>



| <span data-ttu-id="cc2cb-110">欄位</span><span class="sxs-lookup"><span data-stu-id="cc2cb-110">Field</span></span> | <span data-ttu-id="cc2cb-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="cc2cb-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="cc2cb-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cc2cb-112">\[1\]</span></span> | <span data-ttu-id="cc2cb-113">已註冊類型程式庫的[GUID](guid.md) 。</span><span class="sxs-lookup"><span data-stu-id="cc2cb-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cc2cb-114">備註</span><span class="sxs-lookup"><span data-stu-id="cc2cb-114">Remarks</span></span>

<span data-ttu-id="cc2cb-115">RegisterTypeLibraries 動作需要在 TypeLib 資料表的 Language 欄位中正確撰寫型別程式庫語言。</span><span class="sxs-lookup"><span data-stu-id="cc2cb-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="cc2cb-116">撰寫不正確的語言欄位可能會導致安裝程式無法註冊另一個有效的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="cc2cb-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



