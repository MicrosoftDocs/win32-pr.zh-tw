---
title: '其他語言橫條常數 (Ctfutb .h) '
description: 其他語言 bar 常數會設定語言列的特定屬性。
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385110"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="0a46d-103">其他語言橫條圖常數</span><span class="sxs-lookup"><span data-stu-id="0a46d-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="0a46d-104">其他語言 bar 常數會設定語言列的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="0a46d-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="0a46d-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="0a46d-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="0a46d-106">Description</span><span class="sxs-lookup"><span data-stu-id="0a46d-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="0a46d-107"><dt>**TF \_DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0a46d-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0a46d-108">系統語言列專案應該會顯示為語言設定檔指定的圖示。</span><span class="sxs-lookup"><span data-stu-id="0a46d-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="0a46d-109">用於 [ITfSystemDeviceTypeLangBarItem：： GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) 和 [ITfSystemDeviceTypeLangBarItem：： SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) 方法。</span><span class="sxs-lookup"><span data-stu-id="0a46d-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="0a46d-110"><dt>**TF \_INVALIDMENUITEM**</dt> <dt> (UINT)  (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="0a46d-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="0a46d-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="0a46d-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="0a46d-112"><dt>**TF \_LBI \_ BMPF \_ 垂直**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0a46d-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="0a46d-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="0a46d-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="0a46d-114"><dt>**TF \_LBI \_ DESC \_ MAXLEN**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="0a46d-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="0a46d-115">結構成員 [TF \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)的長度（以 WCHAR 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0a46d-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="0a46d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a46d-116">Requirements</span></span>



| <span data-ttu-id="0a46d-117">需求</span><span class="sxs-lookup"><span data-stu-id="0a46d-117">Requirement</span></span> | <span data-ttu-id="0a46d-118">值</span><span class="sxs-lookup"><span data-stu-id="0a46d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a46d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a46d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a46d-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a46d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0a46d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a46d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a46d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a46d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a46d-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0a46d-123">Redistributable</span></span><br/>          | <span data-ttu-id="0a46d-124">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="0a46d-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="0a46d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0a46d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a46d-126"><dt>Ctfutb。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a46d-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a46d-127">Idl</span><span class="sxs-lookup"><span data-stu-id="0a46d-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a46d-128"><dt>Ctfutb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a46d-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a46d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a46d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a46d-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span><span class="sxs-lookup"><span data-stu-id="0a46d-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="0a46d-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span><span class="sxs-lookup"><span data-stu-id="0a46d-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="0a46d-132">TF \_ LANGBARITEMINFO</span><span class="sxs-lookup"><span data-stu-id="0a46d-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





