---
title: Win32_RDSHCollection 類別
description: 管理遠端桌面工作階段主機的集合。
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection 類別遠端桌面服務
- Win32_RDSHCollection 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465549"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="15384-105">Win32 \_ RDSHCollection 類別</span><span class="sxs-lookup"><span data-stu-id="15384-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="15384-106">管理遠端桌面工作階段主機的集合。</span><span class="sxs-lookup"><span data-stu-id="15384-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="15384-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="15384-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15384-108">語法</span><span class="sxs-lookup"><span data-stu-id="15384-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="15384-109">成員</span><span class="sxs-lookup"><span data-stu-id="15384-109">Members</span></span>

<span data-ttu-id="15384-110">**Win32 \_ RDSHCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15384-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="15384-111">方法</span><span class="sxs-lookup"><span data-stu-id="15384-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="15384-112">屬性</span><span class="sxs-lookup"><span data-stu-id="15384-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15384-113">方法</span><span class="sxs-lookup"><span data-stu-id="15384-113">Methods</span></span>

<span data-ttu-id="15384-114">**Win32 \_ RDSHCollection** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="15384-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="15384-115">方法</span><span class="sxs-lookup"><span data-stu-id="15384-115">Method</span></span>                                                                      | <span data-ttu-id="15384-116">描述</span><span class="sxs-lookup"><span data-stu-id="15384-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15384-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="15384-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="15384-118">抓取 **Win32 \_ RDSHCollection** 物件的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="15384-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="15384-119">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="15384-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="15384-120">抓取 **Win32 \_ RDSHCollection** 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="15384-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="15384-121">**KeyValueCompareAndSet**</span><span class="sxs-lookup"><span data-stu-id="15384-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="15384-122">比較集合中指定的索引鍵與比較元;如果相符，索引鍵會設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="15384-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="15384-123">如果索引鍵不存在，方法會將索引鍵插入集合中。</span><span class="sxs-lookup"><span data-stu-id="15384-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="15384-124">**KeyValueDelete**</span><span class="sxs-lookup"><span data-stu-id="15384-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="15384-125">從集合中刪除指定的索引鍵 (以及相關聯的值) 。</span><span class="sxs-lookup"><span data-stu-id="15384-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="15384-126">**KeyValueGet**</span><span class="sxs-lookup"><span data-stu-id="15384-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="15384-127">抓取與集合中指定之索引鍵相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="15384-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="15384-128">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="15384-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="15384-129">更新 **Win32 \_ RDSHCollection** 物件的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="15384-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="15384-130">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="15384-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="15384-131">更新 **Win32 \_ RDSHCollection** 物件的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="15384-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="15384-132">屬性</span><span class="sxs-lookup"><span data-stu-id="15384-132">Properties</span></span>

<span data-ttu-id="15384-133">**Win32 \_ RDSHCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="15384-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15384-134">**別名**</span><span class="sxs-lookup"><span data-stu-id="15384-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15384-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15384-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15384-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="15384-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15384-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15384-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15384-138">取得和設定集合的別名。</span><span class="sxs-lookup"><span data-stu-id="15384-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="15384-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="15384-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15384-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15384-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15384-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="15384-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15384-142">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15384-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15384-143">取得和設定集合的描述。</span><span class="sxs-lookup"><span data-stu-id="15384-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="15384-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="15384-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15384-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15384-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15384-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="15384-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15384-147">取得和設定集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="15384-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="15384-148">**型別**</span><span class="sxs-lookup"><span data-stu-id="15384-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15384-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15384-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15384-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="15384-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15384-151">**Windows server 2012 R2 和 Windows server 2012：** 此屬性在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="15384-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="15384-152">集合的類型。</span><span class="sxs-lookup"><span data-stu-id="15384-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="15384-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**一般** (0) </span><span class="sxs-lookup"><span data-stu-id="15384-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="15384-154">(2)</span><span class="sxs-lookup"><span data-stu-id="15384-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="15384-155">保留</span><span class="sxs-lookup"><span data-stu-id="15384-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="15384-156">(3)</span><span class="sxs-lookup"><span data-stu-id="15384-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="15384-157">保留</span><span class="sxs-lookup"><span data-stu-id="15384-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="15384-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4) </span><span class="sxs-lookup"><span data-stu-id="15384-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="15384-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5) </span><span class="sxs-lookup"><span data-stu-id="15384-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="15384-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="15384-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="15384-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="15384-161">Requirements</span></span>



| <span data-ttu-id="15384-162">需求</span><span class="sxs-lookup"><span data-stu-id="15384-162">Requirement</span></span> | <span data-ttu-id="15384-163">值</span><span class="sxs-lookup"><span data-stu-id="15384-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="15384-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15384-164">Minimum supported client</span></span><br/> | <span data-ttu-id="15384-165">都不支援</span><span class="sxs-lookup"><span data-stu-id="15384-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="15384-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15384-166">Minimum supported server</span></span><br/> | <span data-ttu-id="15384-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15384-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="15384-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="15384-168">Namespace</span></span><br/>                | <span data-ttu-id="15384-169">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="15384-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="15384-170">MOF</span><span class="sxs-lookup"><span data-stu-id="15384-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15384-171"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="15384-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="15384-172">DLL</span><span class="sxs-lookup"><span data-stu-id="15384-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15384-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15384-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="15384-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15384-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15384-175">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="15384-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

