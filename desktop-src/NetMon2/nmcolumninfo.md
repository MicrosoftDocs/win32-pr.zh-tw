---
description: NMCOLUMNINFO 結構會在事件檢視器的上方窗格中定義一個資料行。
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: 'NMCOLUMNINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986611"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="7f9f2-103">NMCOLUMNINFO 結構</span><span class="sxs-lookup"><span data-stu-id="7f9f2-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="7f9f2-104">**NMCOLUMNINFO** 結構會在事件檢視器的上方窗格中定義一個資料行。</span><span class="sxs-lookup"><span data-stu-id="7f9f2-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f9f2-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="7f9f2-106">成員</span><span class="sxs-lookup"><span data-stu-id="7f9f2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f9f2-107">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="7f9f2-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="7f9f2-108">特定資料行的可顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7f9f2-108">Displayable name of a specific column.</span></span> <span data-ttu-id="7f9f2-109">如果名稱太長，就不會在預設的事件檢視器設定中完全顯示。</span><span class="sxs-lookup"><span data-stu-id="7f9f2-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7f9f2-110">**VariantData**</span><span class="sxs-lookup"><span data-stu-id="7f9f2-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="7f9f2-111">插入資料行中的資料。</span><span class="sxs-lookup"><span data-stu-id="7f9f2-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f9f2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f9f2-112">Requirements</span></span>



| <span data-ttu-id="7f9f2-113">需求</span><span class="sxs-lookup"><span data-stu-id="7f9f2-113">Requirement</span></span> | <span data-ttu-id="7f9f2-114">值</span><span class="sxs-lookup"><span data-stu-id="7f9f2-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9f2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f9f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7f9f2-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f9f2-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f9f2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f9f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7f9f2-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f9f2-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f9f2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7f9f2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f9f2-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="7f9f2-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




