---
description: 開啟或關閉全螢幕應用程式時，通知 appbar。 此通知是以應用程式定義的訊息形式傳送，此訊息是由 ABM 的 \_ 新訊息所設定。
title: 'ABN_FULLSCREENAPP 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112360"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="50549-104">ABN \_ FULLSCREENAPP 訊息</span><span class="sxs-lookup"><span data-stu-id="50549-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="50549-105">開啟或關閉全螢幕應用程式時，通知 appbar。</span><span class="sxs-lookup"><span data-stu-id="50549-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="50549-106">此通知是以應用程式定義的訊息形式傳送，此訊息是由 ABM 的 [**\_ 新**](abm-new.md) 訊息所設定。</span><span class="sxs-lookup"><span data-stu-id="50549-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="50549-107">參數</span><span class="sxs-lookup"><span data-stu-id="50549-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50549-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="50549-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="50549-109">指定全螢幕應用程式是否開啟或關閉的旗標。</span><span class="sxs-lookup"><span data-stu-id="50549-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="50549-110">如果應用程式是開啟的，則此參數為 **TRUE** ，如果關閉，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="50549-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50549-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="50549-111">Return value</span></span>

<span data-ttu-id="50549-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="50549-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50549-113">備註</span><span class="sxs-lookup"><span data-stu-id="50549-113">Remarks</span></span>

<span data-ttu-id="50549-114">開啟全螢幕應用程式時，appbar 必須放到迭置順序的底部。</span><span class="sxs-lookup"><span data-stu-id="50549-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="50549-115">當它關閉時，appbar 應該會還原其 z 順序位置。</span><span class="sxs-lookup"><span data-stu-id="50549-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="50549-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="50549-116">Requirements</span></span>



| <span data-ttu-id="50549-117">需求</span><span class="sxs-lookup"><span data-stu-id="50549-117">Requirement</span></span> | <span data-ttu-id="50549-118">值</span><span class="sxs-lookup"><span data-stu-id="50549-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50549-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50549-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50549-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50549-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50549-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50549-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50549-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50549-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50549-123">標頭</span><span class="sxs-lookup"><span data-stu-id="50549-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50549-124"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="50549-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




