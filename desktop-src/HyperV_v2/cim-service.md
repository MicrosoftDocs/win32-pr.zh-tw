---
description: 代表邏輯元素，其中包含代表和管理裝置或軟體功能所提供之功能的資訊。
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: 'CIM_Service 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970204"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="c4419-103">CIM_Service 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="c4419-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="c4419-104">代表邏輯元素，其中包含代表和管理裝置或軟體功能所提供之功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="c4419-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="c4419-105">服務是一般用途的物件，用來設定及管理功能的執行;這並不是功能本身。</span><span class="sxs-lookup"><span data-stu-id="c4419-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4419-106">語法</span><span class="sxs-lookup"><span data-stu-id="c4419-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="c4419-107">成員</span><span class="sxs-lookup"><span data-stu-id="c4419-107">Members</span></span>

<span data-ttu-id="c4419-108">**CIM \_ 服務** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c4419-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="c4419-109">方法</span><span class="sxs-lookup"><span data-stu-id="c4419-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4419-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c4419-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4419-111">方法</span><span class="sxs-lookup"><span data-stu-id="c4419-111">Methods</span></span>

<span data-ttu-id="c4419-112">**CIM \_ 服務** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c4419-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="c4419-113">方法</span><span class="sxs-lookup"><span data-stu-id="c4419-113">Method</span></span>                                           | <span data-ttu-id="c4419-114">描述</span><span class="sxs-lookup"><span data-stu-id="c4419-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="c4419-115">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c4419-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="c4419-116">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="c4419-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="c4419-117">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c4419-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="c4419-118">停止服務。</span><span class="sxs-lookup"><span data-stu-id="c4419-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="c4419-119">屬性</span><span class="sxs-lookup"><span data-stu-id="c4419-119">Properties</span></span>

<span data-ttu-id="c4419-120">**CIM \_ 服務** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c4419-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4419-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4419-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4419-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4419-124">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="c4419-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4419-125">用來建立這個類別之實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c4419-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="c4419-126">**CreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別和其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c4419-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="c4419-127">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c4419-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4419-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4419-130">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="c4419-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4419-131">服務的唯一識別碼，表示服務的功能。</span><span class="sxs-lookup"><span data-stu-id="c4419-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4419-132">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c4419-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c4419-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4419-135">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="c4419-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="c4419-136">服務主要擁有者的連絡人資訊。</span><span class="sxs-lookup"><span data-stu-id="c4419-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4419-137">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="c4419-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c4419-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4419-140">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="c4419-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c4419-141">服務主要擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4419-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4419-142">**已開始**</span><span class="sxs-lookup"><span data-stu-id="c4419-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c4419-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4419-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4419-145">如果服務已啟動，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="c4419-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="c4419-146">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c4419-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4419-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4419-149">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ 服務**」。**EnabledDefault**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="c4419-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c4419-150">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="c4419-150">This property is deprecated.</span></span> <span data-ttu-id="c4419-151">請改用繼承自 [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)的 **EnabledDefault** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c4419-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="c4419-152">已淘汰的描述：指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="c4419-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="c4419-153"> ( "Automatic" ) </span><span class="sxs-lookup"><span data-stu-id="c4419-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c4419-154"> ( 「手動」 ) </span><span class="sxs-lookup"><span data-stu-id="c4419-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4419-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4419-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4419-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4419-158">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="c4419-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="c4419-159">用來建立包含服務之系統實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c4419-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="c4419-160">**SystemCreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別及其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c4419-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="c4419-161">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c4419-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4419-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c4419-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4419-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c4419-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4419-164">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="c4419-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="c4419-165">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4419-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4419-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4419-166">Requirements</span></span>



| <span data-ttu-id="c4419-167">需求</span><span class="sxs-lookup"><span data-stu-id="c4419-167">Requirement</span></span> | <span data-ttu-id="c4419-168">值</span><span class="sxs-lookup"><span data-stu-id="c4419-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4419-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4419-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c4419-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c4419-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c4419-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4419-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c4419-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4419-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c4419-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="c4419-173">Namespace</span></span><br/>                | <span data-ttu-id="c4419-174">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c4419-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4419-175">MOF</span><span class="sxs-lookup"><span data-stu-id="c4419-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4419-176"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c4419-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4419-177">DLL</span><span class="sxs-lookup"><span data-stu-id="c4419-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4419-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4419-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4419-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4419-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4419-180">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c4419-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

