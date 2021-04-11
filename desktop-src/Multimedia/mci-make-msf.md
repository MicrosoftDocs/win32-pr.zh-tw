---
title: 'MCI_MAKE_MSF 宏 (Mciapi) '
description: MCI \_ 讓 \_ msf 宏在指定的分鐘數、秒數和框架值中，以壓縮的分鐘/秒/框架來建立時間值 (MSF) 格式。
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935069"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="b0a9b-104">MCI \_ MAKE \_ MSF 宏</span><span class="sxs-lookup"><span data-stu-id="b0a9b-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="b0a9b-105">**MCI \_ 讓 \_ msf** 宏在指定的分鐘數、秒數和框架值中，以壓縮的分鐘/秒/框架來建立時間值 (MSF) 格式。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a9b-106">語法</span><span class="sxs-lookup"><span data-stu-id="b0a9b-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="b0a9b-107">參數</span><span class="sxs-lookup"><span data-stu-id="b0a9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0a9b-108">*分鐘*</span><span class="sxs-lookup"><span data-stu-id="b0a9b-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="b0a9b-109">分鐘數。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="b0a9b-110">*seconds*</span><span class="sxs-lookup"><span data-stu-id="b0a9b-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="b0a9b-111">秒數。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="b0a9b-112">*框架*</span><span class="sxs-lookup"><span data-stu-id="b0a9b-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="b0a9b-113">畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0a9b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0a9b-114">Return value</span></span>

<span data-ttu-id="b0a9b-115">傳回壓縮 MSF 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a9b-116">備註</span><span class="sxs-lookup"><span data-stu-id="b0a9b-116">Remarks</span></span>

<span data-ttu-id="b0a9b-117">MSF 格式的時程表示為 **DWORD** 值，具有最小的最小位元組數（包含分鐘）、下一個最不重要的位元組（包含秒），以及下一個包含框架的最小有效位元組。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="b0a9b-118">最重要的位元組未使用。</span><span class="sxs-lookup"><span data-stu-id="b0a9b-118">The most significant byte is unused.</span></span>

<span data-ttu-id="b0a9b-119">**MCI \_ MAKE \_ MSF** 巨集定義如下：</span><span class="sxs-lookup"><span data-stu-id="b0a9b-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="b0a9b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0a9b-120">Requirements</span></span>



| <span data-ttu-id="b0a9b-121">需求</span><span class="sxs-lookup"><span data-stu-id="b0a9b-121">Requirement</span></span> | <span data-ttu-id="b0a9b-122">值</span><span class="sxs-lookup"><span data-stu-id="b0a9b-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a9b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0a9b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a9b-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0a9b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0a9b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0a9b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a9b-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0a9b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0a9b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b0a9b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0a9b-128"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0a9b-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0a9b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0a9b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a9b-130">Mci</span><span class="sxs-lookup"><span data-stu-id="b0a9b-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b0a9b-131">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="b0a9b-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





