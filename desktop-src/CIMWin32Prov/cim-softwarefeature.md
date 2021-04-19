---
description: CIM \_ SoftwareFeature 類別代表產品或應用程式系統的特定功能或功能。
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: CIM_SoftwareFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999829"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="a67bf-103">CIM \_ SoftwareFeature 類別</span><span class="sxs-lookup"><span data-stu-id="a67bf-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="a67bf-104">**CIM \_ SoftwareFeature** 類別代表產品或應用程式系統的特定功能或功能。</span><span class="sxs-lookup"><span data-stu-id="a67bf-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="a67bf-105">此類別會反映對產品使用者有意義的資料細微性層級，而不是反映使用 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 類別) 所捕捉的產品建立或封裝 (的單位。</span><span class="sxs-lookup"><span data-stu-id="a67bf-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="a67bf-106">當軟體功能可以存在於多個平臺或作業系統時，「軟體」功能是適用于不同平臺的軟體元素集合。</span><span class="sxs-lookup"><span data-stu-id="a67bf-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="a67bf-107">在這種情況下，模型的使用者通常會對特定平臺所需的軟體元素子集合感興趣。</span><span class="sxs-lookup"><span data-stu-id="a67bf-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="a67bf-108">因為功能是透過產品傳遞，所以軟體功能一律會使用 [**cim \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md)關聯在 [**cim \_ 產品**](cim-product.md)類別的內容中定義。</span><span class="sxs-lookup"><span data-stu-id="a67bf-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="a67bf-109">（選擇性）您可以使用 [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) 關聯，將一或多個產品中的軟體功能組織成應用程式系統。</span><span class="sxs-lookup"><span data-stu-id="a67bf-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a67bf-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a67bf-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a67bf-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a67bf-112">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a67bf-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a67bf-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a67bf-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a67bf-114">語法</span><span class="sxs-lookup"><span data-stu-id="a67bf-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="a67bf-115">成員</span><span class="sxs-lookup"><span data-stu-id="a67bf-115">Members</span></span>

<span data-ttu-id="a67bf-116">**CIM \_ SoftwareFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a67bf-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="a67bf-117">屬性</span><span class="sxs-lookup"><span data-stu-id="a67bf-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a67bf-118">屬性</span><span class="sxs-lookup"><span data-stu-id="a67bf-118">Properties</span></span>

<span data-ttu-id="a67bf-119">**CIM \_ SoftwareFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a67bf-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a67bf-120">**標題**</span><span class="sxs-lookup"><span data-stu-id="a67bf-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-123">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-124">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="a67bf-124">Short textual description of the object.</span></span>

<span data-ttu-id="a67bf-125">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-126">**說明**</span><span class="sxs-lookup"><span data-stu-id="a67bf-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-129">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-130">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a67bf-130">Textual description of the object.</span></span>

<span data-ttu-id="a67bf-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="a67bf-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-135">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**IdentifyingNumber**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="a67bf-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-136">產品識別，例如軟體上的序號或硬體晶片上的骰子編號。</span><span class="sxs-lookup"><span data-stu-id="a67bf-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a67bf-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a67bf-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="a67bf-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-141">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a67bf-141">Date and time the object was installed.</span></span> <span data-ttu-id="a67bf-142">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="a67bf-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a67bf-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a67bf-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-147">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a67bf-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-148">資料處理系統外部已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a67bf-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="a67bf-149">標籤是人類看得懂的名稱，可唯一識別元素命名空間內容中的元素。</span><span class="sxs-lookup"><span data-stu-id="a67bf-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="a67bf-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="a67bf-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-154">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Name**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="a67bf-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-155">常用的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="a67bf-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-156">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a67bf-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-159">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-160">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a67bf-160">Current status of the object.</span></span>

<span data-ttu-id="a67bf-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a67bf-162">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="a67bf-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a67bf-163">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a67bf-164">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a67bf-165">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a67bf-166">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a67bf-167">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a67bf-168">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a67bf-169">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a67bf-170">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a67bf-171">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a67bf-172">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a67bf-173">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a67bf-174">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="a67bf-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a67bf-175">**廠商**</span><span class="sxs-lookup"><span data-stu-id="a67bf-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-178">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**廠商**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="a67bf-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-179">產品供應商的名稱，其對應至「DMTF 解決方案交換標準」產品物件中的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a67bf-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="a67bf-180">**版本**</span><span class="sxs-lookup"><span data-stu-id="a67bf-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a67bf-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a67bf-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a67bf-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a67bf-183">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Version**") 、 [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="a67bf-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a67bf-184">產品版本資訊，對應至 [DMTF 解決方案交換標準] 產品物件中的 [ **版本** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="a67bf-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a67bf-185">備註</span><span class="sxs-lookup"><span data-stu-id="a67bf-185">Remarks</span></span>

<span data-ttu-id="a67bf-186">**Cim \_ SoftwareFeature** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a67bf-187">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a67bf-187">WMI does not implement this class.</span></span> <span data-ttu-id="a67bf-188">針對衍生自 **CIM \_ SOFTWAREFEATURE** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="a67bf-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a67bf-189">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a67bf-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a67bf-190">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a67bf-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a67bf-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="a67bf-191">Requirements</span></span>



| <span data-ttu-id="a67bf-192">需求</span><span class="sxs-lookup"><span data-stu-id="a67bf-192">Requirement</span></span> | <span data-ttu-id="a67bf-193">值</span><span class="sxs-lookup"><span data-stu-id="a67bf-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a67bf-194">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a67bf-194">Minimum supported client</span></span><br/> | <span data-ttu-id="a67bf-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a67bf-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a67bf-196">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a67bf-196">Minimum supported server</span></span><br/> | <span data-ttu-id="a67bf-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a67bf-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a67bf-198">命名空間</span><span class="sxs-lookup"><span data-stu-id="a67bf-198">Namespace</span></span><br/>                | <span data-ttu-id="a67bf-199">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a67bf-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a67bf-200">MOF</span><span class="sxs-lookup"><span data-stu-id="a67bf-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a67bf-201"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a67bf-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a67bf-202">DLL</span><span class="sxs-lookup"><span data-stu-id="a67bf-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a67bf-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a67bf-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a67bf-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a67bf-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67bf-205">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a67bf-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

