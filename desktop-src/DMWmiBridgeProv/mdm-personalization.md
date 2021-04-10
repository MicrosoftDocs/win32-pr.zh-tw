---
title: MDM_Personalization 類別
description: MDM \_ 個人化類別是用來設定鎖定畫面和桌面背景影像。 設定這些原則也可防止使用者變更映射。
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- MDM_Personalization 類別
- MDM_Personalization 類別，描述
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934181"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="86341-106">MDM \_ 個人化類別</span><span class="sxs-lookup"><span data-stu-id="86341-106">MDM\_Personalization class</span></span>

<span data-ttu-id="86341-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="86341-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="86341-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="86341-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="86341-109">MDM \_ 個人化類別是用來設定鎖定畫面和桌面背景影像。</span><span class="sxs-lookup"><span data-stu-id="86341-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="86341-110">設定這些原則也可防止使用者變更映射。</span><span class="sxs-lookup"><span data-stu-id="86341-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="86341-111">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="86341-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="86341-112">語法</span><span class="sxs-lookup"><span data-stu-id="86341-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="86341-113">成員</span><span class="sxs-lookup"><span data-stu-id="86341-113">Members</span></span>

<span data-ttu-id="86341-114">**MDM \_ 個人** 化類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86341-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="86341-115">屬性</span><span class="sxs-lookup"><span data-stu-id="86341-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86341-116">屬性</span><span class="sxs-lookup"><span data-stu-id="86341-116">Properties</span></span>

<span data-ttu-id="86341-117">**MDM \_ 個人** 化類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86341-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="86341-118">DesktopImageStatus</span><span class="sxs-lookup"><span data-stu-id="86341-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="86341-119">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="86341-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="86341-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86341-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="86341-121">DesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="86341-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="86341-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86341-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86341-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86341-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86341-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="86341-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86341-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86341-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86341-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86341-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86341-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="86341-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="86341-128">LockScreenImageStatus</span><span class="sxs-lookup"><span data-stu-id="86341-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="86341-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="86341-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="86341-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86341-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="86341-131">LockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="86341-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="86341-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86341-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86341-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86341-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86341-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="86341-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86341-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86341-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86341-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86341-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86341-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="86341-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86341-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="86341-138">Requirements</span></span>



| <span data-ttu-id="86341-139">需求</span><span class="sxs-lookup"><span data-stu-id="86341-139">Requirement</span></span> | <span data-ttu-id="86341-140">值</span><span class="sxs-lookup"><span data-stu-id="86341-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86341-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86341-141">Minimum supported client</span></span><br/> | <span data-ttu-id="86341-142">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86341-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86341-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86341-143">Minimum supported server</span></span><br/> | <span data-ttu-id="86341-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="86341-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="86341-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="86341-145">Namespace</span></span><br/>                | <span data-ttu-id="86341-146">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="86341-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="86341-147">MOF</span><span class="sxs-lookup"><span data-stu-id="86341-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86341-148"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="86341-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="86341-149">DLL</span><span class="sxs-lookup"><span data-stu-id="86341-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86341-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86341-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

