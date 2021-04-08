---
title: 'IADsPath 屬性方法 (Iads .h) '
description: IADsPath 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- IADsPath 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686203"
---
# <a name="iadspath-property-methods"></a><span data-ttu-id="bcea1-105">IADsPath 屬性方法</span><span class="sxs-lookup"><span data-stu-id="bcea1-105">IADsPath Property Methods</span></span>

<span data-ttu-id="bcea1-106">[**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="bcea1-106">The property method of the [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) interface sets the property described in the following table.</span></span> <span data-ttu-id="bcea1-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="bcea1-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="bcea1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="bcea1-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="bcea1-109">**路徑**</span><span class="sxs-lookup"><span data-stu-id="bcea1-109">**Path**</span></span>
<span data-ttu-id="bcea1-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcea1-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcea1-111">檔案系統目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="bcea1-111">Path of a directory of the file system.</span></span>

<dt>

<span data-ttu-id="bcea1-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bcea1-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcea1-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bcea1-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcea1-114">**型別**</span><span class="sxs-lookup"><span data-stu-id="bcea1-114">**Type**</span></span>
<span data-ttu-id="bcea1-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcea1-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcea1-116">檔案系統的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="bcea1-116">File type of the file system.</span></span>

<dt>

<span data-ttu-id="bcea1-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bcea1-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcea1-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="bcea1-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bcea1-119">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="bcea1-119">**VolumeName**</span></span>
<span data-ttu-id="bcea1-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bcea1-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="bcea1-121">檔案系統現有磁片區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcea1-121">Name of an existing volume of the file system.</span></span>

<dt>

<span data-ttu-id="bcea1-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bcea1-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bcea1-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bcea1-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="bcea1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcea1-124">Requirements</span></span>



| <span data-ttu-id="bcea1-125">需求</span><span class="sxs-lookup"><span data-stu-id="bcea1-125">Requirement</span></span> | <span data-ttu-id="bcea1-126">值</span><span class="sxs-lookup"><span data-stu-id="bcea1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcea1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcea1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bcea1-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcea1-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcea1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcea1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bcea1-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcea1-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcea1-131">標頭</span><span class="sxs-lookup"><span data-stu-id="bcea1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcea1-132"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="bcea1-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="bcea1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bcea1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcea1-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcea1-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="bcea1-135">IID</span><span class="sxs-lookup"><span data-stu-id="bcea1-135">IID</span></span><br/>                      | <span data-ttu-id="bcea1-136">IID \_ IADsPath 定義為 B287FCD5-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="bcea1-136">IID\_IADsPath is defined as B287FCD5-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bcea1-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcea1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcea1-138">**IADsPath**</span><span class="sxs-lookup"><span data-stu-id="bcea1-138">**IADsPath**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[<span data-ttu-id="bcea1-139">**ADS \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="bcea1-139">**ADS\_PATH**</span></span>](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





