---
title: MDM_Policy_Config01_ErrorReporting02 類別
description: MDM \_ Policy \_ Config01 ErrorReporting02 類別會設定 \_ 錯誤報表原則。
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- MDM_Policy_Config01_ErrorReporting02 類別
- MDM_Policy_Config01_ErrorReporting02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024899"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="99fe8-105">MDM \_ 原則 \_ Config01 \_ ErrorReporting02 類別</span><span class="sxs-lookup"><span data-stu-id="99fe8-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="99fe8-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="99fe8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="99fe8-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="99fe8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="99fe8-108">MDM \_ Policy \_ Config01 ErrorReporting02 類別會設定 \_ 錯誤報表原則。</span><span class="sxs-lookup"><span data-stu-id="99fe8-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="99fe8-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="99fe8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="99fe8-110">語法</span><span class="sxs-lookup"><span data-stu-id="99fe8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="99fe8-111">成員</span><span class="sxs-lookup"><span data-stu-id="99fe8-111">Members</span></span>

<span data-ttu-id="99fe8-112">**MDM \_ Policy \_ Config01 \_ ErrorReporting02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="99fe8-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="99fe8-113">屬性</span><span class="sxs-lookup"><span data-stu-id="99fe8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99fe8-114">屬性</span><span class="sxs-lookup"><span data-stu-id="99fe8-114">Properties</span></span>

<span data-ttu-id="99fe8-115">**MDM \_ Policy \_ Config01 \_ ErrorReporting02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="99fe8-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="99fe8-116">CustomizeConsentSettings</span><span class="sxs-lookup"><span data-stu-id="99fe8-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="99fe8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="99fe8-119">DisableWindowsErrorReporting</span><span class="sxs-lookup"><span data-stu-id="99fe8-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="99fe8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="99fe8-122">DisplayErrorNotification</span><span class="sxs-lookup"><span data-stu-id="99fe8-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="99fe8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="99fe8-125">DoNotSendAdditionalData</span><span class="sxs-lookup"><span data-stu-id="99fe8-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="99fe8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="99fe8-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="99fe8-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99fe8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="99fe8-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="99fe8-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="99fe8-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99fe8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="99fe8-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="99fe8-136">PreventCriticalErrorDisplay</span><span class="sxs-lookup"><span data-stu-id="99fe8-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="99fe8-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="99fe8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99fe8-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="99fe8-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99fe8-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="99fe8-139">Requirements</span></span>



| <span data-ttu-id="99fe8-140">需求</span><span class="sxs-lookup"><span data-stu-id="99fe8-140">Requirement</span></span> | <span data-ttu-id="99fe8-141">值</span><span class="sxs-lookup"><span data-stu-id="99fe8-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99fe8-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99fe8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="99fe8-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99fe8-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99fe8-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99fe8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="99fe8-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="99fe8-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="99fe8-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="99fe8-146">Namespace</span></span><br/>                | <span data-ttu-id="99fe8-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="99fe8-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="99fe8-148">MOF</span><span class="sxs-lookup"><span data-stu-id="99fe8-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99fe8-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="99fe8-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="99fe8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="99fe8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99fe8-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99fe8-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

