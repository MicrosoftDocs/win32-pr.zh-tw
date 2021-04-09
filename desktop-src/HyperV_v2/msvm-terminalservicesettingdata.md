---
description: 代表主機上虛擬電腦終端機服務的設定。
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Msvm_TerminalServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691456"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="c2f4c-103">Msvm \_ TerminalServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="c2f4c-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="c2f4c-104">代表主機上虛擬電腦終端機服務的設定。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="c2f4c-105">無法直接修改這個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="c2f4c-106">用戶端必須呼叫 [**Msvm \_ TerminalService. ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) 方法來修改任何這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="c2f4c-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f4c-108">語法</span><span class="sxs-lookup"><span data-stu-id="c2f4c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="c2f4c-109">成員</span><span class="sxs-lookup"><span data-stu-id="c2f4c-109">Members</span></span>

<span data-ttu-id="c2f4c-110">**Msvm \_ TerminalServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c2f4c-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c2f4c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c2f4c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2f4c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c2f4c-112">Properties</span></span>

<span data-ttu-id="c2f4c-113">**Msvm \_ TerminalServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2f4c-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-115">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c2f4c-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-117">驗證同盟驗證權杖簽章所接受的雜湊演算法清單。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="c2f4c-118">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-119">**AuthCertificateHash**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-120">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="c2f4c-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-122">要用於遠端驗證之憑證的雜湊。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-123">**標題**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-126">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-126">A short description of the object.</span></span> <span data-ttu-id="c2f4c-127">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-131">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-131">A description of the object.</span></span> <span data-ttu-id="c2f4c-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-133">**DisableSelfSignedCertificateGeneration**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-136">停用自我簽署憑證產生。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-140">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-140">A display name for the object.</span></span> <span data-ttu-id="c2f4c-141">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-145">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-146">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c2f4c-147">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-148">**ListenerPort**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-151">將在其上進行初始遠端會話連接的網路埠。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="c2f4c-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="c2f4c-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f4c-153">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c2f4c-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2f4c-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2f4c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f4c-155">驗證同盟驗證權杖簽章的受信任簽發者憑證雜湊清單。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="c2f4c-156">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="c2f4c-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2f4c-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2f4c-157">Requirements</span></span>



| <span data-ttu-id="c2f4c-158">需求</span><span class="sxs-lookup"><span data-stu-id="c2f4c-158">Requirement</span></span> | <span data-ttu-id="c2f4c-159">值</span><span class="sxs-lookup"><span data-stu-id="c2f4c-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f4c-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2f4c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f4c-161">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2f4c-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c2f4c-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2f4c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f4c-163">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2f4c-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2f4c-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="c2f4c-164">Namespace</span></span><br/>                | <span data-ttu-id="c2f4c-165">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c2f4c-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c2f4c-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c2f4c-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2f4c-167"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c2f4c-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2f4c-168">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f4c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f4c-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2f4c-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

