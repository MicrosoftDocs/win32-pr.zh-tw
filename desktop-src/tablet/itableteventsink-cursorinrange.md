---
description: 手寫筆進入數位板的偵測範圍內時發生。
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: ITabletEventSink：： CursorInRange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975938"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="604b3-103">ITabletEventSink：： CursorInRange 方法</span><span class="sxs-lookup"><span data-stu-id="604b3-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="604b3-104">手寫筆進入數位板的偵測範圍內時發生。</span><span class="sxs-lookup"><span data-stu-id="604b3-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="604b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="604b3-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="604b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="604b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604b3-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="604b3-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="604b3-108">偵測到手寫筆的 tablet 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="604b3-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="604b3-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="604b3-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="604b3-110">在數位板的範圍內的手寫筆物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="604b3-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604b3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="604b3-111">Return value</span></span>

<span data-ttu-id="604b3-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="604b3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="604b3-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="604b3-113">Return code</span></span>                                                                            | <span data-ttu-id="604b3-114">Description</span><span class="sxs-lookup"><span data-stu-id="604b3-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="604b3-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="604b3-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="604b3-116">成功。</span><span class="sxs-lookup"><span data-stu-id="604b3-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="604b3-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="604b3-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="604b3-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="604b3-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="604b3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="604b3-119">Requirements</span></span>



| <span data-ttu-id="604b3-120">需求</span><span class="sxs-lookup"><span data-stu-id="604b3-120">Requirement</span></span> | <span data-ttu-id="604b3-121">值</span><span class="sxs-lookup"><span data-stu-id="604b3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="604b3-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="604b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="604b3-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="604b3-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="604b3-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="604b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="604b3-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="604b3-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="604b3-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="604b3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="604b3-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="604b3-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604b3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="604b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604b3-129">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="604b3-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




