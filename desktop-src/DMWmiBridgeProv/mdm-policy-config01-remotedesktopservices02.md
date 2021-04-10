---
title: MDM_Policy_Config01_RemoteDesktopServices02 類別
description: MDM \_ Policy \_ Config01 RemoteDesktopServices02 類別會設定 \_ 遠端桌面服務原則。
ms.assetid: d2c53be7-6dec-4603-b851-e9c979475496
keywords:
- MDM_Policy_Config01_RemoteDesktopServices02 類別
- MDM_Policy_Config01_RemoteDesktopServices02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteDesktopServices02
- MDM_Policy_Config01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Config01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a023ae44c7b8ab170d4efe9c38aaacdeca3cc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934354"
---
# <a name="mdm_policy_config01_remotedesktopservices02-class"></a><span data-ttu-id="e613a-105">MDM \_ 原則 \_ Config01 \_ RemoteDesktopServices02 類別</span><span class="sxs-lookup"><span data-stu-id="e613a-105">MDM\_Policy\_Config01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="e613a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e613a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e613a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e613a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e613a-108">MDM \_ Policy \_ Config01 RemoteDesktopServices02 類別會設定 \_ 遠端桌面服務原則。</span><span class="sxs-lookup"><span data-stu-id="e613a-108">The MDM\_Policy\_Config01\_RemoteDesktopServices02 class configures the remote desktop service policies.</span></span>

<span data-ttu-id="e613a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e613a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e613a-110">語法</span><span class="sxs-lookup"><span data-stu-id="e613a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="e613a-111">成員</span><span class="sxs-lookup"><span data-stu-id="e613a-111">Members</span></span>

<span data-ttu-id="e613a-112">**MDM \_ Policy \_ Config01 \_ RemoteDesktopServices02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e613a-112">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="e613a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e613a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e613a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e613a-114">Properties</span></span>

<span data-ttu-id="e613a-115">**MDM \_ Policy \_ Config01 \_ RemoteDesktopServices02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e613a-115">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e613a-116">AllowUsersToConnectRemotely</span><span class="sxs-lookup"><span data-stu-id="e613a-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e613a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e613a-119">ClientConnectionEncryptionLevel</span><span class="sxs-lookup"><span data-stu-id="e613a-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e613a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e613a-122">DoNotAllowDriveRedirection</span><span class="sxs-lookup"><span data-stu-id="e613a-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e613a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e613a-125">DoNotAllowPasswordSaving</span><span class="sxs-lookup"><span data-stu-id="e613a-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e613a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e613a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e613a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e613a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e613a-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e613a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e613a-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e613a-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e613a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e613a-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e613a-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e613a-136">PromptForPasswordUponConnection</span><span class="sxs-lookup"><span data-stu-id="e613a-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e613a-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e613a-139">RequireSecureRPCCommunication</span><span class="sxs-lookup"><span data-stu-id="e613a-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e613a-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e613a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e613a-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e613a-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e613a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="e613a-142">Requirements</span></span>



| <span data-ttu-id="e613a-143">需求</span><span class="sxs-lookup"><span data-stu-id="e613a-143">Requirement</span></span> | <span data-ttu-id="e613a-144">值</span><span class="sxs-lookup"><span data-stu-id="e613a-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e613a-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e613a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e613a-146">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e613a-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e613a-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e613a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e613a-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="e613a-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e613a-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="e613a-149">Namespace</span></span><br/>                | <span data-ttu-id="e613a-150">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e613a-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e613a-151">MOF</span><span class="sxs-lookup"><span data-stu-id="e613a-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e613a-152"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e613a-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e613a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e613a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e613a-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e613a-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

