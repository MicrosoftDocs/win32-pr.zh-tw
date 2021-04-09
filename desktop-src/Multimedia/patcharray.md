---
title: 'PATCHARRAY (Mmsystem) '
description: PATCHARRAY 是一種用來定義 MIDI 修補程式陣列的型別。
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844396"
---
# <a name="patcharray"></a><span data-ttu-id="6138d-104">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="6138d-104">PATCHARRAY</span></span>

<span data-ttu-id="6138d-105">PATCHARRAY 是一種用來定義 MIDI 修補程式陣列的型別。</span><span class="sxs-lookup"><span data-stu-id="6138d-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="6138d-106">**PATCHARRAY \[ MIDIPATCHSIZE\]**</span><span class="sxs-lookup"><span data-stu-id="6138d-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="6138d-107">陣列中的每個元素都會對應到一個 patch，其中每個16位代表16個 MIDI 通道的其中一個。</span><span class="sxs-lookup"><span data-stu-id="6138d-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="6138d-108">系統會為每個使用該特定修補程式的通道設定 Bits。</span><span class="sxs-lookup"><span data-stu-id="6138d-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="6138d-109">例如，如果實體 MIDI 通道0和8使用 patch number 0，則陣列的元素0應該設定為0x0101。</span><span class="sxs-lookup"><span data-stu-id="6138d-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6138d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6138d-110">Requirements</span></span>



| <span data-ttu-id="6138d-111">需求</span><span class="sxs-lookup"><span data-stu-id="6138d-111">Requirement</span></span> | <span data-ttu-id="6138d-112">值</span><span class="sxs-lookup"><span data-stu-id="6138d-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6138d-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6138d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6138d-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6138d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6138d-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6138d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6138d-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6138d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6138d-117">版本</span><span class="sxs-lookup"><span data-stu-id="6138d-117">Version</span></span><br/>                  | <span data-ttu-id="6138d-118">音樂檢測數位介面 (MIDI) 、MIDI 類型</span><span class="sxs-lookup"><span data-stu-id="6138d-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="6138d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="6138d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6138d-120"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6138d-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6138d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6138d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6138d-122">MIDI 類型</span><span class="sxs-lookup"><span data-stu-id="6138d-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





