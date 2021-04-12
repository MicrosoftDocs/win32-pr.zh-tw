---
title: MDM_ActiveSync_User_Options03 類別
description: MDM \_ ActiveSync \_ 使用者 \_ Options03 類別會定義為每個 ActiveSync 帳戶設定的選項。
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- MDM_ActiveSync_User_Options03 類別
- MDM_ActiveSync_User_Options03 類別，描述
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094407"
---
# <a name="mdm_activesync_user_options03-class"></a><span data-ttu-id="b572a-105">MDM \_ ActiveSync \_ 使用者 \_ Options03 類別</span><span class="sxs-lookup"><span data-stu-id="b572a-105">MDM\_ActiveSync\_User\_Options03 class</span></span>

<span data-ttu-id="b572a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b572a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b572a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b572a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b572a-108">**MDM \_ ActiveSync \_ 使用者 \_ Options03** 類別會定義為每個 ActiveSync 帳戶設定的選項。</span><span class="sxs-lookup"><span data-stu-id="b572a-108">The **MDM\_ActiveSync\_User\_Options03** class defines the options that are set for each ActiveSync account.</span></span>

<span data-ttu-id="b572a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b572a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b572a-110">語法</span><span class="sxs-lookup"><span data-stu-id="b572a-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a><span data-ttu-id="b572a-111">成員</span><span class="sxs-lookup"><span data-stu-id="b572a-111">Members</span></span>

<span data-ttu-id="b572a-112">**MDM \_ ActiveSync \_ 使用者 \_ Options03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b572a-112">The **MDM\_ActiveSync\_User\_Options03** class has these types of members:</span></span>

-   [<span data-ttu-id="b572a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b572a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b572a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b572a-114">Properties</span></span>

<span data-ttu-id="b572a-115">**MDM \_ ActiveSync \_ 使用者 \_ Options03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b572a-115">The **MDM\_ActiveSync\_User\_Options03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b572a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b572a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b572a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b572a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b572a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b572a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b572a-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b572a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b572a-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b572a-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="b572a-121">Logging</span><span class="sxs-lookup"><span data-stu-id="b572a-121">Logging</span></span>](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b572a-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b572a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b572a-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b572a-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b572a-124">MailAgeFilter</span><span class="sxs-lookup"><span data-stu-id="b572a-124">MailAgeFilter</span></span>](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b572a-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b572a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b572a-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b572a-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b572a-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b572a-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b572a-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b572a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b572a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b572a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b572a-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b572a-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b572a-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b572a-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="b572a-132">此類別的字串為 "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span><span class="sxs-lookup"><span data-stu-id="b572a-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span></span>

</dd> <dt>

<span data-ttu-id="b572a-133">[[排程]](/windows/client-management/mdm/activesync-csp#options-schedule)</span><span class="sxs-lookup"><span data-stu-id="b572a-133">[Schedule](/windows/client-management/mdm/activesync-csp#options-schedule)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b572a-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b572a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b572a-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b572a-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b572a-136">UseSSL</span><span class="sxs-lookup"><span data-stu-id="b572a-136">UseSSL</span></span>](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b572a-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b572a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b572a-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b572a-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b572a-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b572a-139">Requirements</span></span>



| <span data-ttu-id="b572a-140">需求</span><span class="sxs-lookup"><span data-stu-id="b572a-140">Requirement</span></span> | <span data-ttu-id="b572a-141">值</span><span class="sxs-lookup"><span data-stu-id="b572a-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b572a-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b572a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b572a-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b572a-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b572a-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b572a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b572a-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="b572a-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b572a-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="b572a-146">Namespace</span></span><br/>                | <span data-ttu-id="b572a-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b572a-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b572a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b572a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b572a-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b572a-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b572a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b572a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b572a-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b572a-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b572a-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b572a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b572a-153">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="b572a-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

