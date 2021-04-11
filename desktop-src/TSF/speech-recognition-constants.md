---
title: '語音辨識常數 (Ctffunc .h) '
description: 下列值適用于語音辨識文字服務。
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093964"
---
# <a name="speech-recognition-constants"></a><span data-ttu-id="d0c9c-103">語音辨識常數</span><span class="sxs-lookup"><span data-stu-id="d0c9c-103">Speech Recognition Constants</span></span>

<span data-ttu-id="d0c9c-104">下列值適用于語音辨識文字服務。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-104">The following values are used with the speech recognition text service.</span></span>



| <span data-ttu-id="d0c9c-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="d0c9c-105">Constant/value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="d0c9c-106">Description</span><span class="sxs-lookup"><span data-stu-id="d0c9c-106">Description</span></span>                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <span data-ttu-id="d0c9c-107"><dt>**TF \_0x00000001 \_ 上的聽寫**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-107"><dt>**TF\_DICTATION\_ON**</dt> <dt>0x00000001</dt></span></span> </dl>                   | <span data-ttu-id="d0c9c-108">如果此位為1，則語音聽寫為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-108">If this bit is 1, speech dictation is active.</span></span> <span data-ttu-id="d0c9c-109">否則，語音聽寫為非使用中。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-109">Otherwise, speech dictation is inactive.</span></span> <span data-ttu-id="d0c9c-110">這個值無法與中的 TF \_ 命令結合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-110">This value cannot be combined with TF\_COMMANDING\_ON.</span></span> <span data-ttu-id="d0c9c-111">搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-111">Used with the [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment.</span></span><br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <span data-ttu-id="d0c9c-112"><dt>**TF \_聽寫 \_ 已啟用**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-112"><dt>**TF\_DICTATION\_ENABLED**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="d0c9c-113">如果此位為1，則會啟用語音聽寫。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-113">If this bit is 1, speech dictation is enabled.</span></span> <span data-ttu-id="d0c9c-114">否則，就會停用語音聽寫。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-114">Otherwise, speech dictation is disabled.</span></span> <span data-ttu-id="d0c9c-115">搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-115">Used with the [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment.</span></span><br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <span data-ttu-id="d0c9c-116"><dt>**TF \_命令 \_ 啟用**</dt>的 <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-116"><dt>**TF\_COMMANDING\_ENABLED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="d0c9c-117">如果此位為1，則會啟用語音命令。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-117">If this bit is 1, speech command is enabled.</span></span> <span data-ttu-id="d0c9c-118">否則，會停用語音命令。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-118">Otherwise, speech command is disabled.</span></span> <span data-ttu-id="d0c9c-119">搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-119">Used with the [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment.</span></span><br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <span data-ttu-id="d0c9c-120"><dt>**TF \_\_在0x00000008 上命令**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-120"><dt>**TF\_COMMANDING\_ON**</dt> <dt>0x00000008</dt></span></span> </dl>                | <span data-ttu-id="d0c9c-121">如果此位為1，則語音命令為使用中。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-121">If this bit is 1, speech command is active.</span></span> <span data-ttu-id="d0c9c-122">否則，語音命令為非作用中。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-122">Otherwise, speech command is inactive.</span></span> <span data-ttu-id="d0c9c-123">此值不能與的 TF \_ 聽寫合併 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-123">This value cannot be combined with TF\_DICTATION\_ON.</span></span> <span data-ttu-id="d0c9c-124">搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-124">Used with the [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment.</span></span><br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <span data-ttu-id="d0c9c-125"><dt>**TF \_SPEECHUI \_ 顯示**</dt>的 <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-125"><dt>**TF\_SPEECHUI\_SHOWN**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="d0c9c-126">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-126">Not currently used.</span></span><br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <span data-ttu-id="d0c9c-127"><dt>**TF \_顯示 \_ 氣球**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-127"><dt>**TF\_SHOW\_BALLOON**</dt> <dt>0x00000001</dt></span></span> </dl>                   | <span data-ttu-id="d0c9c-128">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-128">Not currently used.</span></span> <span data-ttu-id="d0c9c-129">搭配 GUID 區間 [ \_ \_ 語音 \_ UI \_ 狀態](predefined-compartments.md) 區間使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-129">Used with the [GUID\_COMPARTMENT\_SPEECH\_UI\_STATUS](predefined-compartments.md) compartment.</span></span><br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <span data-ttu-id="d0c9c-130"><dt>**TF \_停用 \_ 氣球**</dt>的 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-130"><dt>**TF\_DISABLE\_BALLOON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="d0c9c-131">如果這個位為1，表示目前語音模式的氣球顯示已停用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-131">If this bit is 1, balloon display for the current speech mode is disabled.</span></span> <span data-ttu-id="d0c9c-132">否則，會啟用目前語音模式的氣球顯示。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-132">Otherwise, balloon display for the current speech mode is enabled.</span></span> <span data-ttu-id="d0c9c-133">搭配 GUID 區間 [ \_ \_ 語音 \_ UI \_ 狀態](predefined-compartments.md) 區間使用。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-133">Used with the [GUID\_COMPARTMENT\_SPEECH\_UI\_STATUS](predefined-compartments.md) compartment.</span></span><br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <span data-ttu-id="d0c9c-134"><dt>**TF \_停用 \_ 語音**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-134"><dt>**TF\_DISABLE\_SPEECH**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="d0c9c-135">如果此位為1，則會停用語音輸入。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-135">If this bit is 1, speech input is disabled.</span></span> <span data-ttu-id="d0c9c-136">否則，會啟用語音輸入。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-136">Otherwise, speech input is enabled.</span></span> <span data-ttu-id="d0c9c-137">搭配使用 [GUID 區間 \_ \_ 語音 \_ 停](predefined-compartments.md) 用區間。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-137">Used with the [GUID\_COMPARTMENT\_SPEECH\_DISABLED](predefined-compartments.md) compartment.</span></span><br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <span data-ttu-id="d0c9c-138"><dt>**TF \_停用 \_ 聽寫**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-138"><dt>**TF\_DISABLE\_DICTATION**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="d0c9c-139">如果此位為1，則會停用語音聽寫。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-139">If this bit is 1, speech dictation is disabled.</span></span> <span data-ttu-id="d0c9c-140">否則，會啟用語音聽寫。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-140">Otherwise, speech dictation is enabled.</span></span> <span data-ttu-id="d0c9c-141">搭配使用 [GUID 區間 \_ \_ 語音 \_ 停](predefined-compartments.md) 用區間。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-141">Used with the [GUID\_COMPARTMENT\_SPEECH\_DISABLED](predefined-compartments.md) compartment.</span></span><br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <span data-ttu-id="d0c9c-142"><dt>**TF \_停用 \_ 命令**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-142"><dt>**TF\_DISABLE\_COMMANDING**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="d0c9c-143">如果此位為1，則會停用 [語音] 命令。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-143">If this bit is 1, speech command is disabled.</span></span> <span data-ttu-id="d0c9c-144">否則，會啟用語音命令。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-144">Otherwise, speech command is enabled.</span></span> <span data-ttu-id="d0c9c-145">搭配使用 [GUID 區間 \_ \_ 語音 \_ 停](predefined-compartments.md) 用區間。</span><span class="sxs-lookup"><span data-stu-id="d0c9c-145">Used with the [GUID\_COMPARTMENT\_SPEECH\_DISABLED](predefined-compartments.md) compartment.</span></span><br/>                                                                |



## <a name="requirements"></a><span data-ttu-id="d0c9c-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0c9c-146">Requirements</span></span>



| <span data-ttu-id="d0c9c-147">需求</span><span class="sxs-lookup"><span data-stu-id="d0c9c-147">Requirement</span></span> | <span data-ttu-id="d0c9c-148">值</span><span class="sxs-lookup"><span data-stu-id="d0c9c-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c9c-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0c9c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c9c-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0c9c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d0c9c-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0c9c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c9c-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0c9c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                    |
| <span data-ttu-id="d0c9c-153">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d0c9c-153">Redistributable</span></span><br/>          | <span data-ttu-id="d0c9c-154">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="d0c9c-154">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                                                                                         |
| <span data-ttu-id="d0c9c-155">標頭</span><span class="sxs-lookup"><span data-stu-id="d0c9c-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c9c-156"><dt>Ctffunc .h;</dt><dt>Msctf .h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-156"><dt>Ctffunc.h; </dt> <dt>Msctf.h</dt></span></span> </dl>     |
| <span data-ttu-id="d0c9c-157">Idl</span><span class="sxs-lookup"><span data-stu-id="d0c9c-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0c9c-158"><dt>Ctffunc .idl;</dt><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0c9c-158"><dt>Ctffunc.idl; </dt> <dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c9c-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0c9c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c9c-160">預先定義的區間</span><span class="sxs-lookup"><span data-stu-id="d0c9c-160">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

 





