---
title: 'HKM_SETRULES 訊息 (Commctrl .h) '
description: 定義快速鍵控制項的無效組合和預設輔助按鍵組合。
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES message Windows 控制項
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465693"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="fcaa7-104">HKM \_ SETRULES 訊息</span><span class="sxs-lookup"><span data-stu-id="fcaa7-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="fcaa7-105">定義快速鍵控制項的無效組合和預設輔助按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcaa7-106">參數</span><span class="sxs-lookup"><span data-stu-id="fcaa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcaa7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcaa7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcaa7-108">旗標的陣列，指定不正確按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="fcaa7-109">這個參數可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="fcaa7-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="fcaa7-110">值</span><span class="sxs-lookup"><span data-stu-id="fcaa7-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="fcaa7-111">意義</span><span class="sxs-lookup"><span data-stu-id="fcaa7-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="fcaa7-112"><dt>**HKCOMB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="fcaa7-113">ALT</span><span class="sxs-lookup"><span data-stu-id="fcaa7-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="fcaa7-114"><dt>**HKCOMB \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="fcaa7-115">CTRL</span><span class="sxs-lookup"><span data-stu-id="fcaa7-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="fcaa7-116"><dt>**HKCOMB \_ CA**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="fcaa7-117">CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="fcaa7-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="fcaa7-118"><dt>**HKCOMB \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="fcaa7-119">未修改的金鑰</span><span class="sxs-lookup"><span data-stu-id="fcaa7-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="fcaa7-120"><dt>**HKCOMB \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="fcaa7-121">SHIFT</span><span class="sxs-lookup"><span data-stu-id="fcaa7-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="fcaa7-122"><dt>**HKCOMB \_ SA**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="fcaa7-123">SHIFT+ALT</span><span class="sxs-lookup"><span data-stu-id="fcaa7-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="fcaa7-124"><dt>**HKCOMB \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="fcaa7-125">SHIFT + CTRL</span><span class="sxs-lookup"><span data-stu-id="fcaa7-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="fcaa7-126"><dt>**HKCOMB \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="fcaa7-127">SHIFT + CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="fcaa7-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="fcaa7-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcaa7-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcaa7-129">旗標的陣列，指定當使用者輸入不正確組合時，所要使用的按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="fcaa7-130">如需修飾詞旗標值的清單，請參閱 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息的說明。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcaa7-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcaa7-131">Return value</span></span>

<span data-ttu-id="fcaa7-132">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcaa7-133">備註</span><span class="sxs-lookup"><span data-stu-id="fcaa7-133">Remarks</span></span>

<span data-ttu-id="fcaa7-134">當使用者輸入不正確按鍵組合（如 *wParam* 中所指定的旗標所定義）時，系統會使用位 or 運算子，將使用者輸入的索引鍵與 *lParam* 中指定的旗標合併。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="fcaa7-135">產生的按鍵組合會轉換成字串，然後顯示在快速鍵控制項中。</span><span class="sxs-lookup"><span data-stu-id="fcaa7-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcaa7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcaa7-136">Requirements</span></span>



| <span data-ttu-id="fcaa7-137">需求</span><span class="sxs-lookup"><span data-stu-id="fcaa7-137">Requirement</span></span> | <span data-ttu-id="fcaa7-138">值</span><span class="sxs-lookup"><span data-stu-id="fcaa7-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcaa7-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcaa7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fcaa7-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcaa7-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcaa7-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcaa7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fcaa7-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcaa7-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcaa7-143">標頭</span><span class="sxs-lookup"><span data-stu-id="fcaa7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcaa7-144"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fcaa7-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





