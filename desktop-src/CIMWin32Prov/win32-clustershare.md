---
description: Win32 \_ ClusterShare 類別代表叢集中的共用資源。
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111237"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="31d46-103">Win32 \_ ClusterShare 類別</span><span class="sxs-lookup"><span data-stu-id="31d46-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="31d46-104">\[**Win32 \_ ClusterShare** 類別已被取代。</span><span class="sxs-lookup"><span data-stu-id="31d46-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="31d46-105">請改用 [**msft 檔案 \_ 共用**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) 和 [**msft \_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) 類別。\]</span><span class="sxs-lookup"><span data-stu-id="31d46-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="31d46-106">Win32 \_ ClusterShare 類別代表叢集中的共用資源。</span><span class="sxs-lookup"><span data-stu-id="31d46-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="31d46-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="31d46-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d46-108">語法</span><span class="sxs-lookup"><span data-stu-id="31d46-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="31d46-109">成員</span><span class="sxs-lookup"><span data-stu-id="31d46-109">Members</span></span>

<span data-ttu-id="31d46-110">**Win32 \_ ClusterShare** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="31d46-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="31d46-111">方法</span><span class="sxs-lookup"><span data-stu-id="31d46-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="31d46-112">屬性</span><span class="sxs-lookup"><span data-stu-id="31d46-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31d46-113">方法</span><span class="sxs-lookup"><span data-stu-id="31d46-113">Methods</span></span>

<span data-ttu-id="31d46-114">**Win32 \_ ClusterShare** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="31d46-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="31d46-115">方法</span><span class="sxs-lookup"><span data-stu-id="31d46-115">Method</span></span>                                                    | <span data-ttu-id="31d46-116">描述</span><span class="sxs-lookup"><span data-stu-id="31d46-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="31d46-117">**創建**</span><span class="sxs-lookup"><span data-stu-id="31d46-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="31d46-118">建立新的 **Win32 \_ ClusterShare** 實例。</span><span class="sxs-lookup"><span data-stu-id="31d46-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="31d46-119">**刪除**</span><span class="sxs-lookup"><span data-stu-id="31d46-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="31d46-120">刪除 **Win32 \_ ClusterShare** 實例。</span><span class="sxs-lookup"><span data-stu-id="31d46-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="31d46-121">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="31d46-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="31d46-122">傳回具有共用存取權限的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="31d46-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="31d46-123">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="31d46-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="31d46-124">設定共用資源的參數。</span><span class="sxs-lookup"><span data-stu-id="31d46-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="31d46-125">屬性</span><span class="sxs-lookup"><span data-stu-id="31d46-125">Properties</span></span>

<span data-ttu-id="31d46-126">**Win32 \_ ClusterShare** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="31d46-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31d46-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="31d46-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="31d46-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-130">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31d46-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31d46-131">這個屬性已過時，不再使用。</span><span class="sxs-lookup"><span data-stu-id="31d46-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="31d46-132">請改用 [**Win32 \_ GetAccessMask**](getaccessmask-method-in-class-win32-share.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="31d46-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="31d46-133">WMI 會將 **AccessMask** 屬性的值設定為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="31d46-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="31d46-134">如需在建立共用時設定存取權的詳細資訊，請參閱 [**建立**](create-method-in-class-win32-share.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="31d46-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="31d46-135">這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-136">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="31d46-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="31d46-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-140">此資源的並行使用者數目已受限制。</span><span class="sxs-lookup"><span data-stu-id="31d46-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="31d46-141">若 **為 True**，則會忽略 **MaximumAllowed** 屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="31d46-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="31d46-142">這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-143">**標題**</span><span class="sxs-lookup"><span data-stu-id="31d46-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31d46-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-146">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="31d46-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-147">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="31d46-147">A short textual description of the object.</span></span>

<span data-ttu-id="31d46-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-149">**說明**</span><span class="sxs-lookup"><span data-stu-id="31d46-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31d46-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-152">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="31d46-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-153">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="31d46-153">A textual description of the object.</span></span>

<span data-ttu-id="31d46-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31d46-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-156">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="31d46-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-158">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="31d46-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-159">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="31d46-159">Indicates when the object was installed.</span></span> <span data-ttu-id="31d46-160">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="31d46-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="31d46-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="31d46-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="31d46-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-165">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-166">允許同時使用此資源的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="31d46-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="31d46-167">只有當 **AllowMaximum** 屬性設定為 **FALSE** 時，此值才有效。</span><span class="sxs-lookup"><span data-stu-id="31d46-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="31d46-168">這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-169">**名稱**</span><span class="sxs-lookup"><span data-stu-id="31d46-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31d46-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-172">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 網路名稱」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="31d46-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-173">在執行 Windows 的電腦系統上，提供給路徑的別名設定為共用。</span><span class="sxs-lookup"><span data-stu-id="31d46-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="31d46-174">Windows 2008 範例： " \\ SERVER01 \\ public"-windows Server 2008 要求您將 UNC 放在名稱中。</span><span class="sxs-lookup"><span data-stu-id="31d46-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="31d46-175">這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-176">**路徑**</span><span class="sxs-lookup"><span data-stu-id="31d46-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31d46-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-179">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 路徑」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-180">Windows 共用的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="31d46-180">Local path of the Windows share.</span></span>

<span data-ttu-id="31d46-181">範例： "C： \\ Program Files"</span><span class="sxs-lookup"><span data-stu-id="31d46-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="31d46-182">這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="31d46-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="31d46-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31d46-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-186">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ServerName" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| [**SHARE \_ INFO \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName" ) </span><span class="sxs-lookup"><span data-stu-id="31d46-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-187">主控共用的叢集伺服器。</span><span class="sxs-lookup"><span data-stu-id="31d46-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="31d46-188">**狀態**</span><span class="sxs-lookup"><span data-stu-id="31d46-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31d46-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-191">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="31d46-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-192">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="31d46-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="31d46-193">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="31d46-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="31d46-194">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="31d46-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="31d46-195">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="31d46-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="31d46-196">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="31d46-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="31d46-197">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="31d46-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="31d46-198">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="31d46-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="31d46-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="31d46-200">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="31d46-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="31d46-201">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="31d46-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="31d46-202">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31d46-203">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31d46-204">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="31d46-205">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="31d46-206">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="31d46-207">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="31d46-208">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="31d46-209">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="31d46-210">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="31d46-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="31d46-211">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="31d46-212">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31d46-213">**型別**</span><span class="sxs-lookup"><span data-stu-id="31d46-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d46-214">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="31d46-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31d46-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31d46-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d46-216">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 類型」 ) </span><span class="sxs-lookup"><span data-stu-id="31d46-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="31d46-217">共用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="31d46-217">Type of resource being shared.</span></span> <span data-ttu-id="31d46-218">類型包括：磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。</span><span class="sxs-lookup"><span data-stu-id="31d46-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="31d46-219">這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。</span><span class="sxs-lookup"><span data-stu-id="31d46-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="31d46-220">**磁片磁碟機** (0) </span><span class="sxs-lookup"><span data-stu-id="31d46-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="31d46-221">**列印佇列** (1) </span><span class="sxs-lookup"><span data-stu-id="31d46-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="31d46-222">**裝置** (2) </span><span class="sxs-lookup"><span data-stu-id="31d46-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="31d46-223">**IPC** (3) </span><span class="sxs-lookup"><span data-stu-id="31d46-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="31d46-224">**磁片磁碟機系統管理員** (2147483648) </span><span class="sxs-lookup"><span data-stu-id="31d46-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="31d46-225">**列印佇列管理** (2147483649) </span><span class="sxs-lookup"><span data-stu-id="31d46-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="31d46-226">**裝置系統管理員** (2147483650) </span><span class="sxs-lookup"><span data-stu-id="31d46-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="31d46-227">**IPC 系統管理員** (2147483651) </span><span class="sxs-lookup"><span data-stu-id="31d46-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="31d46-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="31d46-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="31d46-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="31d46-229">Requirements</span></span>



| <span data-ttu-id="31d46-230">需求</span><span class="sxs-lookup"><span data-stu-id="31d46-230">Requirement</span></span> | <span data-ttu-id="31d46-231">值</span><span class="sxs-lookup"><span data-stu-id="31d46-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31d46-232">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31d46-232">Minimum supported client</span></span><br/> | <span data-ttu-id="31d46-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31d46-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="31d46-234">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31d46-234">Minimum supported server</span></span><br/> | <span data-ttu-id="31d46-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31d46-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="31d46-236">命名空間</span><span class="sxs-lookup"><span data-stu-id="31d46-236">Namespace</span></span><br/>                | <span data-ttu-id="31d46-237">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="31d46-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31d46-238">MOF</span><span class="sxs-lookup"><span data-stu-id="31d46-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31d46-239"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="31d46-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31d46-240">DLL</span><span class="sxs-lookup"><span data-stu-id="31d46-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d46-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d46-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d46-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31d46-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d46-243">**Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="31d46-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

