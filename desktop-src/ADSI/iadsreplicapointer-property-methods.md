---
title: 'IADsReplicaPointer 屬性方法 (Iads .h) '
description: IADsReplicaPointer 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- IADsReplicaPointer 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508499"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="f3921-105">IADsReplicaPointer 屬性方法</span><span class="sxs-lookup"><span data-stu-id="f3921-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="f3921-106">[**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3921-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="f3921-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="f3921-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f3921-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f3921-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f3921-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="f3921-109">**Count**</span></span>
<span data-ttu-id="f3921-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3921-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3921-111">現有複本的數目。</span><span class="sxs-lookup"><span data-stu-id="f3921-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="f3921-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3921-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3921-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f3921-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3921-114">**ReplicaAddressHints**</span><span class="sxs-lookup"><span data-stu-id="f3921-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="f3921-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3921-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3921-116">建議的網路位址可能是指向名稱伺服器之節點的參考。</span><span class="sxs-lookup"><span data-stu-id="f3921-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="f3921-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3921-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3921-118">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="f3921-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3921-119">**ReplicaNumber**</span><span class="sxs-lookup"><span data-stu-id="f3921-119">**ReplicaNumber**</span></span>
<span data-ttu-id="f3921-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3921-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3921-121">複本的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3921-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="f3921-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3921-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3921-123">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f3921-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3921-124">**ReplicaType**</span><span class="sxs-lookup"><span data-stu-id="f3921-124">**ReplicaType**</span></span>
<span data-ttu-id="f3921-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3921-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3921-126"> (master、次要或唯讀的複本類型。 ) </span><span class="sxs-lookup"><span data-stu-id="f3921-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="f3921-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3921-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3921-128">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f3921-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3921-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="f3921-129">**ServerName**</span></span>
<span data-ttu-id="f3921-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3921-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3921-131">保存複本的名稱伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f3921-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="f3921-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3921-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3921-133">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3921-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="f3921-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3921-134">Requirements</span></span>



| <span data-ttu-id="f3921-135">需求</span><span class="sxs-lookup"><span data-stu-id="f3921-135">Requirement</span></span> | <span data-ttu-id="f3921-136">值</span><span class="sxs-lookup"><span data-stu-id="f3921-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3921-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3921-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f3921-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3921-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3921-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3921-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f3921-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3921-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3921-141">標頭</span><span class="sxs-lookup"><span data-stu-id="f3921-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3921-142"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3921-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f3921-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f3921-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3921-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3921-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3921-145">IID</span><span class="sxs-lookup"><span data-stu-id="f3921-145">IID</span></span><br/>                      | <span data-ttu-id="f3921-146">IID \_ IADsReplicaPointer 定義為 F60FB803-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="f3921-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f3921-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3921-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3921-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="f3921-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="f3921-149">**ADS \_ REPLICAPOINTER**</span><span class="sxs-lookup"><span data-stu-id="f3921-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





