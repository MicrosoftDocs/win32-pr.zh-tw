---
title: 'MPVERSION_INFO 結構 (MpClient .h) '
description: 惡意程式碼防護管理員元件的版本資訊。
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO 結構舊版 Windows 環境功能
- PMPVERSION_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317395"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="639bd-105">MPVERSION \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="639bd-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="639bd-106">惡意程式碼防護管理員元件的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="639bd-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="639bd-107">語法</span><span class="sxs-lookup"><span data-stu-id="639bd-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="639bd-108">成員</span><span class="sxs-lookup"><span data-stu-id="639bd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="639bd-109">**產品**</span><span class="sxs-lookup"><span data-stu-id="639bd-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-110">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-111">產品版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-112">**服務**</span><span class="sxs-lookup"><span data-stu-id="639bd-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-113">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-114">服務元件版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-115">**FileSystemFilter**</span><span class="sxs-lookup"><span data-stu-id="639bd-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-116">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-117">檔案系統篩選元件版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-118">**引擎**</span><span class="sxs-lookup"><span data-stu-id="639bd-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-119">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-120">引擎元件版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-121">**ASSignature**</span><span class="sxs-lookup"><span data-stu-id="639bd-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-122">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-123">防毒軟體簽章元件版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-124">**AVSignature**</span><span class="sxs-lookup"><span data-stu-id="639bd-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-125">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-126">防毒軟體特徵碼元件版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-127">**NISEngine**</span><span class="sxs-lookup"><span data-stu-id="639bd-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-128">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-129">NIS 引擎版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-130">**NISSignature**</span><span class="sxs-lookup"><span data-stu-id="639bd-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-131">類型： **[ **MPCOMPONENT \_ 版本**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="639bd-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-132">NIS 簽名碼元件版本。</span><span class="sxs-lookup"><span data-stu-id="639bd-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="639bd-133">**已保留**</span><span class="sxs-lookup"><span data-stu-id="639bd-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="639bd-134">類型： **[**MPCOMPONENT \_**](mpcomponent-version.md) \[ 第4版\]**</span><span class="sxs-lookup"><span data-stu-id="639bd-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="639bd-135">保留的欄位。</span><span class="sxs-lookup"><span data-stu-id="639bd-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="639bd-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="639bd-136">Requirements</span></span>



| <span data-ttu-id="639bd-137">需求</span><span class="sxs-lookup"><span data-stu-id="639bd-137">Requirement</span></span> | <span data-ttu-id="639bd-138">值</span><span class="sxs-lookup"><span data-stu-id="639bd-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="639bd-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="639bd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="639bd-140">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="639bd-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="639bd-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="639bd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="639bd-142">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="639bd-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="639bd-143">標頭</span><span class="sxs-lookup"><span data-stu-id="639bd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="639bd-144"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="639bd-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="639bd-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="639bd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639bd-146">**MPCOMPONENT \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="639bd-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 





