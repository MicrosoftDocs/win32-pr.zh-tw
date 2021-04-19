---
description: 代表將檔案從主機複製到來賓的參數。
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997918"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="2d0bc-103">Msvm \_ CopyFileToGuestSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="2d0bc-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="2d0bc-104">代表將檔案從主機複製到來賓的參數。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="2d0bc-105">此類別衍生自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="2d0bc-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0bc-107">語法</span><span class="sxs-lookup"><span data-stu-id="2d0bc-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="2d0bc-108">成員</span><span class="sxs-lookup"><span data-stu-id="2d0bc-108">Members</span></span>

<span data-ttu-id="2d0bc-109">**Msvm \_ CopyFileToGuestSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2d0bc-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2d0bc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2d0bc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d0bc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2d0bc-111">Properties</span></span>

<span data-ttu-id="2d0bc-112">**Msvm \_ CopyFileToGuestSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d0bc-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-116">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="2d0bc-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-118">**CreateFullPath**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-121">表示複製檔案之前，是否必須先建立目的地檔案路徑中的遺失目錄。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-129">要複製之目的檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="2d0bc-130">此目的地檔案必須可供來賓存取，而且可以包含環境變數（由來賓展開）。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="2d0bc-131">如果指定的路徑是來賓中的現有目錄，則會在此目錄中建立目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="2d0bc-132">在此情況下， **SourcePath** 的檔案名會用來做為目的地檔案名。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-136">此 SettingData 實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="2d0bc-137">此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="2d0bc-138"> (附注：名稱在命名空間中不一定是唯一的。 ) </span><span class="sxs-lookup"><span data-stu-id="2d0bc-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-142">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-143">在具現化命名空間的範圍內，InstanceID 會以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2d0bc-144">若要確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立： *OrgID*：*LocalID* ，其中 *OrgID* 和 *LocalID* 會以冒號 (： ) ，而且 *OrgID* 必須包含受著作權、商標或其他唯一名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="2d0bc-145"> (這項需求類似于架構類別名稱的 *SchemaName* \_ *ClassName* 結構。 ) 此外，為了確保唯一性， *OrgID* 不能包含冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="2d0bc-146">使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="2d0bc-147">*LocalID* 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="2d0bc-148">如果未使用上述的慣用演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="2d0bc-149">針對 DMTF 定義的實例，您必須使用「慣用」演算法搭配將 *OrgID* 設定為 CIM。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-150">**OverwriteExisting**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-151">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-153">指出是否必須覆寫現有的目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="2d0bc-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0bc-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0bc-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d0bc-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0bc-157">要複製之原始程式檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="2d0bc-158">Hyper-v 主機必須可存取此來源檔案，而且可以包含由 Hyper-v 主機擴充的環境變數。</span><span class="sxs-lookup"><span data-stu-id="2d0bc-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d0bc-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d0bc-159">Requirements</span></span>



| <span data-ttu-id="2d0bc-160">需求</span><span class="sxs-lookup"><span data-stu-id="2d0bc-160">Requirement</span></span> | <span data-ttu-id="2d0bc-161">值</span><span class="sxs-lookup"><span data-stu-id="2d0bc-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0bc-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d0bc-162">Minimum supported client</span></span><br/> | <span data-ttu-id="2d0bc-163">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d0bc-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2d0bc-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d0bc-164">Minimum supported server</span></span><br/> | <span data-ttu-id="2d0bc-165">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d0bc-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d0bc-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d0bc-166">Namespace</span></span><br/>                | <span data-ttu-id="2d0bc-167">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2d0bc-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2d0bc-168">MOF</span><span class="sxs-lookup"><span data-stu-id="2d0bc-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d0bc-169"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2d0bc-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d0bc-170">DLL</span><span class="sxs-lookup"><span data-stu-id="2d0bc-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d0bc-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d0bc-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d0bc-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d0bc-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d0bc-173">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="2d0bc-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="2d0bc-174">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d0bc-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

