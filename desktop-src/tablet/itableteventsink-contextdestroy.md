---
description: 當 tablet 內容終結時發生。
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: ITabletEventSink：： CoNtextDestroy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514016"
---
# <a name="itableteventsinkcontextdestroy-method"></a><span data-ttu-id="0b137-103">ITabletEventSink：： CoNtextDestroy 方法</span><span class="sxs-lookup"><span data-stu-id="0b137-103">ITabletEventSink::ContextDestroy method</span></span>

<span data-ttu-id="0b137-104">當 tablet 內容終結時發生。</span><span class="sxs-lookup"><span data-stu-id="0b137-104">Occurs when a tablet context is being destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b137-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b137-105">Syntax</span></span>


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="0b137-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b137-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b137-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b137-108">要終結的 tablet 內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b137-108">The identifier of the tablet context being destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b137-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b137-109">Return value</span></span>

<span data-ttu-id="0b137-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0b137-110">This method can return one of these values.</span></span>



| <span data-ttu-id="0b137-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0b137-111">Return code</span></span>                                                                            | <span data-ttu-id="0b137-112">Description</span><span class="sxs-lookup"><span data-stu-id="0b137-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0b137-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0b137-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0b137-114">成功。</span><span class="sxs-lookup"><span data-stu-id="0b137-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0b137-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="0b137-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0b137-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b137-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b137-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b137-117">Requirements</span></span>



| <span data-ttu-id="0b137-118">需求</span><span class="sxs-lookup"><span data-stu-id="0b137-118">Requirement</span></span> | <span data-ttu-id="0b137-119">值</span><span class="sxs-lookup"><span data-stu-id="0b137-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b137-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b137-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0b137-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b137-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0b137-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b137-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0b137-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="0b137-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0b137-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b137-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b137-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b137-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b137-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b137-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b137-127">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="0b137-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




