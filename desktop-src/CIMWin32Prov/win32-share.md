---
description: Win32 \_ 共用類別代表執行 Windows 的電腦系統上的共用資源。 這可能是磁片磁碟機、印表機、處理序間通訊或其他可共用的裝置。 如需有關如何抓取 WMI 類別的詳細資訊，請參閱取出類別。
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Win32_Share 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111204"
---
# <a name="win32_share-class"></a><span data-ttu-id="8e37c-105">Win32 \_ 共用類別</span><span class="sxs-lookup"><span data-stu-id="8e37c-105">Win32\_Share class</span></span>

<span data-ttu-id="8e37c-106">**Win32 \_ 共用** 類別代表執行 Windows 的電腦系統上的共用資源。</span><span class="sxs-lookup"><span data-stu-id="8e37c-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="8e37c-107">這可能是磁片磁碟機、印表機、處理序間通訊或其他可共用的裝置。</span><span class="sxs-lookup"><span data-stu-id="8e37c-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="8e37c-108">如需有關如何抓取 WMI 類別的詳細資訊，請參閱 [取出類別](../wmisdk/retrieving-a-class.md)。</span><span class="sxs-lookup"><span data-stu-id="8e37c-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="8e37c-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e37c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e37c-110">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="8e37c-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e37c-111">語法</span><span class="sxs-lookup"><span data-stu-id="8e37c-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="8e37c-112">成員</span><span class="sxs-lookup"><span data-stu-id="8e37c-112">Members</span></span>

<span data-ttu-id="8e37c-113">**Win32 \_ 共用** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e37c-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="8e37c-114">方法</span><span class="sxs-lookup"><span data-stu-id="8e37c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8e37c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8e37c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8e37c-116">方法</span><span class="sxs-lookup"><span data-stu-id="8e37c-116">Methods</span></span>

<span data-ttu-id="8e37c-117">**Win32 \_ 共用** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="8e37c-118">方法</span><span class="sxs-lookup"><span data-stu-id="8e37c-118">Method</span></span>                                                             | <span data-ttu-id="8e37c-119">描述</span><span class="sxs-lookup"><span data-stu-id="8e37c-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e37c-120">**創建**</span><span class="sxs-lookup"><span data-stu-id="8e37c-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="8e37c-121">起始伺服器資源之共用的類別方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="8e37c-122">**刪除**</span><span class="sxs-lookup"><span data-stu-id="8e37c-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="8e37c-123">類別方法，會從伺服器的共用資源清單中刪除共用名稱，中斷與共用資源的連接。</span><span class="sxs-lookup"><span data-stu-id="8e37c-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="8e37c-124">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="8e37c-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="8e37c-125">傳回使用者或群組所持有的共用的存取權限，該共用會傳回該實例。</span><span class="sxs-lookup"><span data-stu-id="8e37c-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="8e37c-126">您應該使用這個方法來取代 **AccessMask** 屬性，此屬性一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8e37c-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="8e37c-127">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="8e37c-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="8e37c-128">設定共用資源的參數的類別方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="8e37c-129">屬性</span><span class="sxs-lookup"><span data-stu-id="8e37c-129">Properties</span></span>

<span data-ttu-id="8e37c-130">**Win32 \_ 共用** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e37c-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e37c-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="8e37c-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e37c-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-134">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e37c-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-135">這個屬性已過時，不再使用。</span><span class="sxs-lookup"><span data-stu-id="8e37c-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="8e37c-136">請改用 [**Win32 \_ GetAccessMask**](getaccessmask-method-in-class-win32-share.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="8e37c-137">WMI 會將 **AccessMask** 屬性的值設定為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="8e37c-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="8e37c-138">如需在建立共用時設定存取權的詳細資訊，請參閱 [**建立**](create-method-in-class-win32-share.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-139">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="8e37c-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e37c-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-142">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-143">此資源的並行使用者數目已受限制。</span><span class="sxs-lookup"><span data-stu-id="8e37c-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="8e37c-144">若 **為 True**，則會忽略 **MaximumAllowed** 屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="8e37c-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-145">**標題**</span><span class="sxs-lookup"><span data-stu-id="8e37c-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e37c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-148">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-149">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="8e37c-149">A short textual description of the object.</span></span>

<span data-ttu-id="8e37c-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e37c-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="8e37c-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e37c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-154">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-155">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="8e37c-155">A textual description of the object.</span></span>

<span data-ttu-id="8e37c-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e37c-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e37c-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-158">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8e37c-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-160">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="8e37c-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-161">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="8e37c-161">Indicates when the object was installed.</span></span> <span data-ttu-id="8e37c-162">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="8e37c-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8e37c-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e37c-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="8e37c-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e37c-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-167">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-168">允許同時使用此資源的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="8e37c-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="8e37c-169">只有當 **AllowMaximum** 屬性設定為 **FALSE** 時，此值才有效。</span><span class="sxs-lookup"><span data-stu-id="8e37c-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-170">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8e37c-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e37c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-173">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**SHARE \_ INFO \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)shi1 網路名稱 \| \_ " ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-174">在執行 Windows 的電腦系統上，提供給路徑的別名設定為共用。</span><span class="sxs-lookup"><span data-stu-id="8e37c-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="8e37c-175">Windows 2008 範例： " \\ SERVER01 \\ public"-windows Server 2008 要求您將 UNC 放在名稱中。</span><span class="sxs-lookup"><span data-stu-id="8e37c-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-176">**路徑**</span><span class="sxs-lookup"><span data-stu-id="8e37c-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e37c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-179">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 路徑」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-180">Windows 共用的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="8e37c-180">Local path of the Windows share.</span></span>

<span data-ttu-id="8e37c-181">範例： "C： \\ Program Files"</span><span class="sxs-lookup"><span data-stu-id="8e37c-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="8e37c-182">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8e37c-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e37c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-185">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-186">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="8e37c-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="8e37c-187">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="8e37c-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8e37c-188">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="8e37c-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8e37c-189">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="8e37c-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8e37c-190">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="8e37c-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e37c-191">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="8e37c-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e37c-192">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="8e37c-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e37c-193">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e37c-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e37c-194">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="8e37c-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e37c-195">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e37c-196">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e37c-197">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e37c-198">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e37c-199">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e37c-200">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e37c-201">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e37c-202">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e37c-203">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e37c-204">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e37c-205">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e37c-206">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e37c-207">**型別**</span><span class="sxs-lookup"><span data-stu-id="8e37c-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e37c-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e37c-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e37c-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e37c-210">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 類型」 ) </span><span class="sxs-lookup"><span data-stu-id="8e37c-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="8e37c-211">共用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8e37c-211">Type of resource being shared.</span></span> <span data-ttu-id="8e37c-212">類型包括：磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。</span><span class="sxs-lookup"><span data-stu-id="8e37c-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="8e37c-213">**磁片磁碟機** (0) </span><span class="sxs-lookup"><span data-stu-id="8e37c-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="8e37c-214">**列印佇列** (1) </span><span class="sxs-lookup"><span data-stu-id="8e37c-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="8e37c-215">**裝置** (2) </span><span class="sxs-lookup"><span data-stu-id="8e37c-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="8e37c-216">**IPC** (3) </span><span class="sxs-lookup"><span data-stu-id="8e37c-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="8e37c-217">**磁片磁碟機系統管理員** (2147483648) </span><span class="sxs-lookup"><span data-stu-id="8e37c-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="8e37c-218">**列印佇列管理** (2147483649) </span><span class="sxs-lookup"><span data-stu-id="8e37c-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="8e37c-219">**裝置系統管理員** (2147483650) </span><span class="sxs-lookup"><span data-stu-id="8e37c-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="8e37c-220">**IPC 系統管理員** (2147483651) </span><span class="sxs-lookup"><span data-stu-id="8e37c-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="8e37c-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8e37c-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8e37c-222">備註</span><span class="sxs-lookup"><span data-stu-id="8e37c-222">Remarks</span></span>

<span data-ttu-id="8e37c-223">**Win32 \_ 共用** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e37c-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="8e37c-224">此類別中的 Create 方法是靜態方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="8e37c-225">**Delete**、 **GetAccessMask** 和 **SetShareInfo** 方法都是實例方法。</span><span class="sxs-lookup"><span data-stu-id="8e37c-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="8e37c-226">根據您的安全性許可權，您可能無法取得此類別的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="8e37c-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="8e37c-227">例如， **AllowMaximum**、 **MaximumAllowed**、 **Path** 和 **Type** 屬性可能會傳回 null。</span><span class="sxs-lookup"><span data-stu-id="8e37c-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="8e37c-228">一般來說，Power Users 和系統管理員將能取得所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="8e37c-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="8e37c-229">範例</span><span class="sxs-lookup"><span data-stu-id="8e37c-229">Examples</span></span>

<span data-ttu-id="8e37c-230">下列腳本中心程式[代碼範例](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) 會列出電腦上的所有共用，並列出每個共用的所有共用許可權。</span><span class="sxs-lookup"><span data-stu-id="8e37c-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="8e37c-231">[Get 共用資訊與 win32 \_ 共用](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c)PowerShell 範例查詢 win32 \_ 共用，並提供結果。</span><span class="sxs-lookup"><span data-stu-id="8e37c-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="8e37c-232">下列 PowerShell 範例會顯示本機系統上的共用。</span><span class="sxs-lookup"><span data-stu-id="8e37c-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="8e37c-233">或者，如果您想要更精確地篩選，您可以使用下列 PowerShell 程式碼片段：</span><span class="sxs-lookup"><span data-stu-id="8e37c-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="8e37c-234">下列 VBScript 範例會顯示本機系統上的共用。</span><span class="sxs-lookup"><span data-stu-id="8e37c-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="8e37c-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e37c-235">Requirements</span></span>



| <span data-ttu-id="8e37c-236">需求</span><span class="sxs-lookup"><span data-stu-id="8e37c-236">Requirement</span></span> | <span data-ttu-id="8e37c-237">值</span><span class="sxs-lookup"><span data-stu-id="8e37c-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e37c-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e37c-238">Minimum supported client</span></span><br/> | <span data-ttu-id="8e37c-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e37c-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e37c-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e37c-240">Minimum supported server</span></span><br/> | <span data-ttu-id="8e37c-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e37c-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e37c-242">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e37c-242">Namespace</span></span><br/>                | <span data-ttu-id="8e37c-243">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e37c-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e37c-244">MOF</span><span class="sxs-lookup"><span data-stu-id="8e37c-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e37c-245"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e37c-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e37c-246">DLL</span><span class="sxs-lookup"><span data-stu-id="8e37c-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e37c-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e37c-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e37c-248">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e37c-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e37c-249">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8e37c-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="8e37c-250">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="8e37c-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8e37c-251">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="8e37c-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
