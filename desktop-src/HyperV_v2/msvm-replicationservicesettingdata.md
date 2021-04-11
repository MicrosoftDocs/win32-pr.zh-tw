---
description: 代表復原主機上複寫服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 Msvm \_ ReplicationService. ModifyServiceSettings 方法來修改任何這些屬性。
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Msvm_ReplicationServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850004"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="f6927-105">Msvm \_ ReplicationServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="f6927-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="f6927-106">代表復原主機上複寫服務的設定。</span><span class="sxs-lookup"><span data-stu-id="f6927-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="f6927-107">無法直接修改這個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6927-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="f6927-108">用戶端必須呼叫 [**Msvm \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) 方法來修改任何這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f6927-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="f6927-109">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6927-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6927-110">語法</span><span class="sxs-lookup"><span data-stu-id="f6927-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="f6927-111">成員</span><span class="sxs-lookup"><span data-stu-id="f6927-111">Members</span></span>

<span data-ttu-id="f6927-112">**Msvm \_ ReplicationServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f6927-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f6927-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f6927-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6927-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f6927-114">Properties</span></span>

<span data-ttu-id="f6927-115">**Msvm \_ ReplicationServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f6927-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6927-116">**AllowedAuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="f6927-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6927-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-119">定義連接到復原主機伺服器時允許的驗證模式。</span><span class="sxs-lookup"><span data-stu-id="f6927-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="f6927-120">0</span><span class="sxs-lookup"><span data-stu-id="f6927-120">0</span></span>
</dt> <dd>

<span data-ttu-id="f6927-121">未定義。</span><span class="sxs-lookup"><span data-stu-id="f6927-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="f6927-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos 驗證** (1) </span><span class="sxs-lookup"><span data-stu-id="f6927-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6927-123">Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="f6927-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="f6927-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>以 **憑證為基礎的驗證** (2) </span><span class="sxs-lookup"><span data-stu-id="f6927-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6927-125">以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="f6927-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="f6927-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>以 **憑證為基礎的驗證和 kerberos 驗證** (3) </span><span class="sxs-lookup"><span data-stu-id="f6927-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6927-127">以憑證為基礎的驗證與整合式驗證。</span><span class="sxs-lookup"><span data-stu-id="f6927-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6927-128">**標題**</span><span class="sxs-lookup"><span data-stu-id="f6927-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6927-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-131">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f6927-131">A short description of the object.</span></span> <span data-ttu-id="f6927-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「複寫服務設定」。</span><span class="sxs-lookup"><span data-stu-id="f6927-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f6927-133">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="f6927-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6927-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6927-136">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128) </span><span class="sxs-lookup"><span data-stu-id="f6927-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="f6927-137">當 **AuthenticationType** 是以憑證為基礎的驗證時，所要使用的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="f6927-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="f6927-138">**說明**</span><span class="sxs-lookup"><span data-stu-id="f6927-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6927-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-141">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f6927-141">A description of the object.</span></span> <span data-ttu-id="f6927-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬機器複寫設定資料」。</span><span class="sxs-lookup"><span data-stu-id="f6927-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="f6927-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f6927-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6927-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-146">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f6927-146">A display name for the object.</span></span> <span data-ttu-id="f6927-147">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「複寫服務設定」。</span><span class="sxs-lookup"><span data-stu-id="f6927-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f6927-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="f6927-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6927-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-151">在接受複寫的非安全連線時，所要使用的復原伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f6927-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="f6927-152">預設值是 80。</span><span class="sxs-lookup"><span data-stu-id="f6927-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="f6927-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="f6927-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6927-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-156">在接受用於複寫的安全連線時，要使用的復原伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f6927-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="f6927-157">預設值為443。</span><span class="sxs-lookup"><span data-stu-id="f6927-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="f6927-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6927-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6927-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6927-161">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f6927-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6927-162">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f6927-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f6927-163">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6927-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6927-164">**MonitoringInterval**</span><span class="sxs-lookup"><span data-stu-id="f6927-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6927-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-167">應該重設複寫統計資料的間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6927-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="f6927-168">預設間隔為12小時 (43200 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f6927-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="f6927-169">最小有效值為60分鐘 (3600 秒) ，最大值為7天 (604800 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f6927-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="f6927-170">**MonitoringStartTime**</span><span class="sxs-lookup"><span data-stu-id="f6927-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-171">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f6927-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-173">複寫監視的開始時間（UTC）。</span><span class="sxs-lookup"><span data-stu-id="f6927-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="f6927-174">預設值為 9:00 A.M.、當地時間，以 UTC 表示。</span><span class="sxs-lookup"><span data-stu-id="f6927-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="f6927-175">**Datetime** 物件的日期元素必須為零。</span><span class="sxs-lookup"><span data-stu-id="f6927-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6927-176">**RecoveryServerEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6927-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6927-177">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6927-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6927-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6927-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6927-179">指定是否將 Hyper-v 主機啟用為復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="f6927-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6927-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6927-180">Requirements</span></span>



| <span data-ttu-id="f6927-181">需求</span><span class="sxs-lookup"><span data-stu-id="f6927-181">Requirement</span></span> | <span data-ttu-id="f6927-182">值</span><span class="sxs-lookup"><span data-stu-id="f6927-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6927-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6927-183">Minimum supported client</span></span><br/> | <span data-ttu-id="f6927-184">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6927-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6927-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6927-185">Minimum supported server</span></span><br/> | <span data-ttu-id="f6927-186">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6927-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6927-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6927-187">Namespace</span></span><br/>                | <span data-ttu-id="f6927-188">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6927-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6927-189">MOF</span><span class="sxs-lookup"><span data-stu-id="f6927-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6927-190"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f6927-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6927-191">DLL</span><span class="sxs-lookup"><span data-stu-id="f6927-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6927-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6927-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6927-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6927-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6927-194">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="f6927-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="f6927-195">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="f6927-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

