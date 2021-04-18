---
title: 'KEYARRAY (Mmsystem) '
description: KEYARRAY 會指定用來定義索引鍵陣列的型別。
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965907"
---
# <a name="keyarray"></a><span data-ttu-id="c2434-104">KEYARRAY</span><span class="sxs-lookup"><span data-stu-id="c2434-104">KEYARRAY</span></span>

<span data-ttu-id="c2434-105">KEYARRAY 會指定用來定義索引鍵陣列的型別。</span><span class="sxs-lookup"><span data-stu-id="c2434-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="c2434-106">**KEYARRAY \[ MIDIPATCHSIZE\]**</span><span class="sxs-lookup"><span data-stu-id="c2434-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="c2434-107">陣列中的每個元素會對應至以金鑰為基礎的 percussion 修補程式，其中每個16位代表16個 MIDI 通道的其中一個。</span><span class="sxs-lookup"><span data-stu-id="c2434-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="c2434-108">系統會為每個使用該特定修補程式的通道設定 Bits。</span><span class="sxs-lookup"><span data-stu-id="c2434-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="c2434-109">例如，如果實體 MIDI 通道9和15使用金鑰編號60的 percussion 修補程式，則應該將陣列的元素60設定為0x8200。</span><span class="sxs-lookup"><span data-stu-id="c2434-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2434-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2434-110">Requirements</span></span>



| <span data-ttu-id="c2434-111">需求</span><span class="sxs-lookup"><span data-stu-id="c2434-111">Requirement</span></span> | <span data-ttu-id="c2434-112">值</span><span class="sxs-lookup"><span data-stu-id="c2434-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2434-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2434-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c2434-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2434-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2434-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2434-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c2434-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2434-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2434-117">版本</span><span class="sxs-lookup"><span data-stu-id="c2434-117">Version</span></span><br/>                  | <span data-ttu-id="c2434-118">音樂檢測數位介面 (MIDI) 、MIDI 類型</span><span class="sxs-lookup"><span data-stu-id="c2434-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="c2434-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c2434-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2434-120"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c2434-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2434-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2434-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2434-122">MIDI 類型</span><span class="sxs-lookup"><span data-stu-id="c2434-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





