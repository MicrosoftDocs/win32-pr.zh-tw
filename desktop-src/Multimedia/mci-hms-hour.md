---
title: 'MCI_HMS_HOUR 宏 (Mciapi) '
description: MCI \_ HMS \_ HOUR 宏會從包含「壓縮的小時/分鐘/秒」參數的參數取出時陣列件 (HMS) 資訊。
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025475"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="90414-104">MCI \_ HMS \_ HOUR 宏</span><span class="sxs-lookup"><span data-stu-id="90414-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="90414-105">**MCI \_ HMS \_ HOUR** 宏會從包含「壓縮的小時/分鐘/秒」參數的參數取出時陣列件 (HMS) 資訊。</span><span class="sxs-lookup"><span data-stu-id="90414-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="90414-106">語法</span><span class="sxs-lookup"><span data-stu-id="90414-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="90414-107">參數</span><span class="sxs-lookup"><span data-stu-id="90414-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90414-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="90414-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="90414-109">HMS 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="90414-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90414-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="90414-110">Return value</span></span>

<span data-ttu-id="90414-111">傳回所指定 HMS 資訊的時陣列件。</span><span class="sxs-lookup"><span data-stu-id="90414-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="90414-112">備註</span><span class="sxs-lookup"><span data-stu-id="90414-112">Remarks</span></span>

<span data-ttu-id="90414-113">HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。</span><span class="sxs-lookup"><span data-stu-id="90414-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="90414-114">最重要的位元組未使用。</span><span class="sxs-lookup"><span data-stu-id="90414-114">The most significant byte is unused.</span></span>

<span data-ttu-id="90414-115">**MCI \_ HMS \_ HOUR** 巨集定義如下：</span><span class="sxs-lookup"><span data-stu-id="90414-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="90414-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="90414-116">Requirements</span></span>



| <span data-ttu-id="90414-117">需求</span><span class="sxs-lookup"><span data-stu-id="90414-117">Requirement</span></span> | <span data-ttu-id="90414-118">值</span><span class="sxs-lookup"><span data-stu-id="90414-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90414-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90414-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90414-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90414-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90414-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90414-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90414-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90414-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="90414-123">標頭</span><span class="sxs-lookup"><span data-stu-id="90414-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90414-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="90414-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90414-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90414-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90414-126">Mci</span><span class="sxs-lookup"><span data-stu-id="90414-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="90414-127">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="90414-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





