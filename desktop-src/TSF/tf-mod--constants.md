---
title: 'TF_MOD_ 常數 (Msctf) '
description: TF \_ MOD \_ \ 常數會指定 tf PRESERVEDKEY 結構中的索引鍵修飾詞 \_ 。
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025057"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="c8390-103">TF \_ MOD \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="c8390-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="c8390-104">TF \_ MOD \_ \* 常數會指定[TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)結構中的索引鍵修飾詞。</span><span class="sxs-lookup"><span data-stu-id="c8390-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="c8390-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="c8390-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="c8390-106">Description</span><span class="sxs-lookup"><span data-stu-id="c8390-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="c8390-107"><dt>**TF \_MOD \_ ALT**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="c8390-108">按下 ALT 鍵的任一個</span><span class="sxs-lookup"><span data-stu-id="c8390-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="c8390-109"><dt>**TF \_MOD \_ 控制項**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="c8390-110">按下 CTRL 鍵的任一個</span><span class="sxs-lookup"><span data-stu-id="c8390-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="c8390-111"><dt>**TF \_MOD \_ 移位**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="c8390-112">按下 SHIFT 鍵的任一個</span><span class="sxs-lookup"><span data-stu-id="c8390-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="c8390-113"><dt>**TF \_MOD \_ RALT**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="c8390-114">按下右邊的 ALT 鍵</span><span class="sxs-lookup"><span data-stu-id="c8390-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="c8390-115"><dt>**TF \_MOD \_ RCONTROL**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="c8390-116">按下右 CTRL 鍵</span><span class="sxs-lookup"><span data-stu-id="c8390-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="c8390-117"><dt>**TF \_MOD \_ RSHIFT**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="c8390-118">按下右移鍵</span><span class="sxs-lookup"><span data-stu-id="c8390-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="c8390-119"><dt>**TF \_MOD \_ LALT**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="c8390-120">左 ALT 鍵已按下</span><span class="sxs-lookup"><span data-stu-id="c8390-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="c8390-121"><dt>**TF \_MOD \_ LCONTROL**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="c8390-122">按下 CTRL 鍵</span><span class="sxs-lookup"><span data-stu-id="c8390-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="c8390-123"><dt>**TF \_MOD \_ LSHIFT**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="c8390-124">已按下左 SHIFT 鍵</span><span class="sxs-lookup"><span data-stu-id="c8390-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="c8390-125"><dt>**TF \_\_在 \_ KEYUP 0x0200 上的 MOD**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8390-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="c8390-126">釋放金鑰時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="c8390-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="c8390-127">如果沒有這個旗標，則會在按下按鍵時引發事件。</span><span class="sxs-lookup"><span data-stu-id="c8390-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="c8390-128"><dt>**TF \_MOD \_ 忽略 \_ 所有 \_ 修飾**</dt>詞 <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="c8390-129">會忽略 ALT、CTRL 和 SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="c8390-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="c8390-130">這表示當按下虛擬機器碼時，就會引發事件，無論按下哪個輔助按鍵。</span><span class="sxs-lookup"><span data-stu-id="c8390-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c8390-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8390-131">Requirements</span></span>



| <span data-ttu-id="c8390-132">需求</span><span class="sxs-lookup"><span data-stu-id="c8390-132">Requirement</span></span> | <span data-ttu-id="c8390-133">值</span><span class="sxs-lookup"><span data-stu-id="c8390-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8390-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8390-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c8390-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8390-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c8390-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8390-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c8390-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8390-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c8390-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c8390-138">Redistributable</span></span><br/>          | <span data-ttu-id="c8390-139">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="c8390-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="c8390-140">標頭</span><span class="sxs-lookup"><span data-stu-id="c8390-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8390-141"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8390-142">Idl</span><span class="sxs-lookup"><span data-stu-id="c8390-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8390-143"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8390-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8390-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8390-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8390-145">TF \_ PRESERVEDKEY</span><span class="sxs-lookup"><span data-stu-id="c8390-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





