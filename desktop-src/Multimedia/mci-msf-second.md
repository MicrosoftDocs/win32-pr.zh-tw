---
title: 'MCI_MSF_SECOND 宏 (Mciapi) '
description: MCI \_ MSF \_ SECOND 宏會從包含壓縮分鐘/秒/框架 (MSF) 資訊的參數抓取秒鐘元件。
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843752"
---
# <a name="mci_msf_second-macro"></a><span data-ttu-id="c5913-104">MCI \_ MSF \_ 第二個宏</span><span class="sxs-lookup"><span data-stu-id="c5913-104">MCI\_MSF\_SECOND macro</span></span>

<span data-ttu-id="c5913-105">**MCI \_ MSF \_ SECOND** 宏會從包含壓縮分鐘/秒/框架 (MSF) 資訊的參數抓取秒鐘元件。</span><span class="sxs-lookup"><span data-stu-id="c5913-105">The **MCI\_MSF\_SECOND** macro retrieves the seconds component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5913-106">語法</span><span class="sxs-lookup"><span data-stu-id="c5913-106">Syntax</span></span>


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="c5913-107">參數</span><span class="sxs-lookup"><span data-stu-id="c5913-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5913-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="c5913-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="c5913-109">MSF 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="c5913-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5913-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5913-110">Return value</span></span>

<span data-ttu-id="c5913-111">傳回指定之 MSF 資訊的秒陣列件。</span><span class="sxs-lookup"><span data-stu-id="c5913-111">Returns the seconds component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5913-112">備註</span><span class="sxs-lookup"><span data-stu-id="c5913-112">Remarks</span></span>

<span data-ttu-id="c5913-113">MSF 格式的時程表示為 **DWORD** 值，具有最小的最小位元組數（包含分鐘）、下一個最不重要的位元組（包含秒），以及下一個包含框架的最小有效位元組。</span><span class="sxs-lookup"><span data-stu-id="c5913-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="c5913-114">最重要的位元組未使用。</span><span class="sxs-lookup"><span data-stu-id="c5913-114">The most significant byte is unused.</span></span>

<span data-ttu-id="c5913-115">**MCI \_ MSF \_ SECOND** 宏的定義如下：</span><span class="sxs-lookup"><span data-stu-id="c5913-115">The **MCI\_MSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="c5913-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5913-116">Requirements</span></span>



| <span data-ttu-id="c5913-117">需求</span><span class="sxs-lookup"><span data-stu-id="c5913-117">Requirement</span></span> | <span data-ttu-id="c5913-118">值</span><span class="sxs-lookup"><span data-stu-id="c5913-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5913-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5913-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5913-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5913-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c5913-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5913-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5913-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5913-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c5913-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c5913-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5913-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5913-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5913-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5913-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5913-126">Mci</span><span class="sxs-lookup"><span data-stu-id="c5913-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c5913-127">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="c5913-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





