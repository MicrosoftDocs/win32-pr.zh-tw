---
title: 'MCI_HMS_MINUTE 宏 (Mciapi) '
description: MCI \_ HMS \_ MINUTE 宏會從包含「壓縮的小時/分鐘/秒」參數的參數抓取分鐘元件 (HMS) 資訊。
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106211"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="39f02-104">MCI \_ HMS \_ MINUTE 宏</span><span class="sxs-lookup"><span data-stu-id="39f02-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="39f02-105">**MCI \_ HMS \_ MINUTE** 宏會從包含「壓縮的小時/分鐘/秒」參數的參數抓取分鐘元件 (HMS) 資訊。</span><span class="sxs-lookup"><span data-stu-id="39f02-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f02-106">語法</span><span class="sxs-lookup"><span data-stu-id="39f02-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="39f02-107">參數</span><span class="sxs-lookup"><span data-stu-id="39f02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f02-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="39f02-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="39f02-109">HMS 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="39f02-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f02-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="39f02-110">Return value</span></span>

<span data-ttu-id="39f02-111">傳回所指定 HMS 資訊的分鐘元件。</span><span class="sxs-lookup"><span data-stu-id="39f02-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f02-112">備註</span><span class="sxs-lookup"><span data-stu-id="39f02-112">Remarks</span></span>

<span data-ttu-id="39f02-113">HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。</span><span class="sxs-lookup"><span data-stu-id="39f02-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="39f02-114">最重要的位元組未使用。</span><span class="sxs-lookup"><span data-stu-id="39f02-114">The most significant byte is unused.</span></span>

<span data-ttu-id="39f02-115">**MCI \_ HMS \_ MINUTE** 巨集定義如下：</span><span class="sxs-lookup"><span data-stu-id="39f02-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="39f02-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="39f02-116">Requirements</span></span>



| <span data-ttu-id="39f02-117">需求</span><span class="sxs-lookup"><span data-stu-id="39f02-117">Requirement</span></span> | <span data-ttu-id="39f02-118">值</span><span class="sxs-lookup"><span data-stu-id="39f02-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39f02-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39f02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39f02-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39f02-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39f02-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39f02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39f02-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39f02-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39f02-123">標頭</span><span class="sxs-lookup"><span data-stu-id="39f02-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39f02-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="39f02-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f02-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39f02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f02-126">Mci</span><span class="sxs-lookup"><span data-stu-id="39f02-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="39f02-127">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="39f02-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





