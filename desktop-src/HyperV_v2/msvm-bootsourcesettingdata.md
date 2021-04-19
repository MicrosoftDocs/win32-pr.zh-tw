---
description: 代表用來設定虛擬機器開機來源的參數。
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974536"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="f4720-103">Msvm \_ BootSourceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="f4720-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="f4720-104">代表用來設定虛擬機器開機來源的參數。</span><span class="sxs-lookup"><span data-stu-id="f4720-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="f4720-105">此類別衍生自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f4720-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="f4720-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4720-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4720-107">語法</span><span class="sxs-lookup"><span data-stu-id="f4720-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="f4720-108">成員</span><span class="sxs-lookup"><span data-stu-id="f4720-108">Members</span></span>

<span data-ttu-id="f4720-109">**Msvm \_ BootSourceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f4720-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f4720-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f4720-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4720-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f4720-111">Properties</span></span>

<span data-ttu-id="f4720-112">**Msvm \_ BootSourceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f4720-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4720-113">**BootSourceDescription**</span><span class="sxs-lookup"><span data-stu-id="f4720-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4720-116">由固件提供的開機來源描述。</span><span class="sxs-lookup"><span data-stu-id="f4720-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="f4720-117">**BootSourceType**</span><span class="sxs-lookup"><span data-stu-id="f4720-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f4720-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4720-120">列舉值，指定開機來源的類型。</span><span class="sxs-lookup"><span data-stu-id="f4720-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="f4720-121">這些是有效的值：</span><span class="sxs-lookup"><span data-stu-id="f4720-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4720-122">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f4720-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="f4720-123">**磁片磁碟機** (1) </span><span class="sxs-lookup"><span data-stu-id="f4720-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="f4720-124">**Network** (2) </span><span class="sxs-lookup"><span data-stu-id="f4720-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="f4720-125">**File** (3) </span><span class="sxs-lookup"><span data-stu-id="f4720-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4720-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="f4720-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4720-129">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="f4720-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f4720-130">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="f4720-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="f4720-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="f4720-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4720-134">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="f4720-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="f4720-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f4720-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4720-138">此 SettingData 實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f4720-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="f4720-139">此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。</span><span class="sxs-lookup"><span data-stu-id="f4720-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="f4720-140"> (附注：名稱在命名空間中不一定是唯一的。 ) </span><span class="sxs-lookup"><span data-stu-id="f4720-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="f4720-141">**FirmwareDevicePath**</span><span class="sxs-lookup"><span data-stu-id="f4720-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4720-144">固件用來描述裝置的原生路徑。</span><span class="sxs-lookup"><span data-stu-id="f4720-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="f4720-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f4720-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4720-148">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f4720-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f4720-149">在具現化命名空間的範圍內，InstanceID 會以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f4720-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f4720-150">若要確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立： *OrgID*：*LocalID* ，其中 *OrgID* 和 *LocalID* 會以冒號 (： ) ，而且 *OrgID* 必須包含受著作權、商標或其他唯一名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4720-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="f4720-151"> (這項需求類似于架構類別名稱的 *SchemaName* \_ *ClassName* 結構。 ) 此外，為了確保唯一性， *OrgID* 不能包含冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="f4720-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="f4720-152">使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="f4720-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="f4720-153">*LocalID* 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。</span><span class="sxs-lookup"><span data-stu-id="f4720-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="f4720-154">如果未使用上述的慣用演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。</span><span class="sxs-lookup"><span data-stu-id="f4720-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="f4720-155">針對 DMTF 定義的實例，您必須使用「慣用」演算法搭配將 *OrgID* 設定為 CIM。</span><span class="sxs-lookup"><span data-stu-id="f4720-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="f4720-156">**OptionalData**</span><span class="sxs-lookup"><span data-stu-id="f4720-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-157">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="f4720-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f4720-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4720-159">限定詞： **OctetString**， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) </span><span class="sxs-lookup"><span data-stu-id="f4720-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="f4720-160">由固件提供的選擇性資料。</span><span class="sxs-lookup"><span data-stu-id="f4720-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="f4720-161">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4720-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f4720-162">**OtherLocation**</span><span class="sxs-lookup"><span data-stu-id="f4720-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4720-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f4720-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4720-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f4720-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4720-165">其他位置資訊（如果有的話），以供固件用來進一步識別開機來源。</span><span class="sxs-lookup"><span data-stu-id="f4720-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4720-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4720-166">Requirements</span></span>



| <span data-ttu-id="f4720-167">需求</span><span class="sxs-lookup"><span data-stu-id="f4720-167">Requirement</span></span> | <span data-ttu-id="f4720-168">值</span><span class="sxs-lookup"><span data-stu-id="f4720-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4720-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4720-169">Minimum supported client</span></span><br/> | <span data-ttu-id="f4720-170">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4720-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f4720-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4720-171">Minimum supported server</span></span><br/> | <span data-ttu-id="f4720-172">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4720-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f4720-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="f4720-173">Namespace</span></span><br/>                | <span data-ttu-id="f4720-174">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f4720-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f4720-175">MOF</span><span class="sxs-lookup"><span data-stu-id="f4720-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4720-176"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f4720-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4720-177">DLL</span><span class="sxs-lookup"><span data-stu-id="f4720-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4720-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4720-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4720-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4720-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4720-180">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="f4720-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="f4720-181">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4720-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

