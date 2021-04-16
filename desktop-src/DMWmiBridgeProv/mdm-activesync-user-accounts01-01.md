---
title: MDM_ActiveSync_User_Accounts01_01 類別
description: MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01 類別會定義所有可用的 ActiveSync 帳戶。
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- MDM_ActiveSync_User_Accounts01_01 類別
- MDM_ActiveSync_User_Accounts01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465021"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="a9274-105">MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="a9274-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="a9274-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a9274-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a9274-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a9274-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a9274-108">**MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01** 類別會定義所有可用的 ActiveSync 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9274-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="a9274-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9274-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9274-110">語法</span><span class="sxs-lookup"><span data-stu-id="a9274-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="a9274-111">成員</span><span class="sxs-lookup"><span data-stu-id="a9274-111">Members</span></span>

<span data-ttu-id="a9274-112">**MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9274-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a9274-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a9274-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9274-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a9274-114">Properties</span></span>

<span data-ttu-id="a9274-115">**MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a9274-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a9274-116">AccountIcon</span><span class="sxs-lookup"><span data-stu-id="a9274-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9274-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="a9274-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9274-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="a9274-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9274-125">網域</span><span class="sxs-lookup"><span data-stu-id="a9274-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9274-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a9274-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9274-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9274-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9274-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9274-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a9274-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a9274-135">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9274-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="a9274-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a9274-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a9274-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9274-139">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a9274-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a9274-140">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a9274-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="a9274-141">此類別的字串為 "./Vendor/MSFT/ActiveSync/"</span><span class="sxs-lookup"><span data-stu-id="a9274-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="a9274-142">密碼</span><span class="sxs-lookup"><span data-stu-id="a9274-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9274-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="a9274-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9274-148">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a9274-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9274-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a9274-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9274-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9274-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9274-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9274-151">Requirements</span></span>



| <span data-ttu-id="a9274-152">需求</span><span class="sxs-lookup"><span data-stu-id="a9274-152">Requirement</span></span> | <span data-ttu-id="a9274-153">值</span><span class="sxs-lookup"><span data-stu-id="a9274-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9274-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9274-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a9274-155">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9274-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9274-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9274-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a9274-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="a9274-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a9274-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="a9274-158">Namespace</span></span><br/>                | <span data-ttu-id="a9274-159">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a9274-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a9274-160">MOF</span><span class="sxs-lookup"><span data-stu-id="a9274-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9274-161"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9274-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9274-162">DLL</span><span class="sxs-lookup"><span data-stu-id="a9274-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9274-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9274-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9274-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9274-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9274-165">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a9274-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

