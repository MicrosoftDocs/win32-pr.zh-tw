---
description: 開啟多個存取的專案。
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'IPStore：： OpenItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999988"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="0958f-103">IPStore：： OpenItem 方法</span><span class="sxs-lookup"><span data-stu-id="0958f-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="0958f-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="0958f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0958f-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="0958f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0958f-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="0958f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0958f-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="0958f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0958f-108">開啟多個存取的專案。</span><span class="sxs-lookup"><span data-stu-id="0958f-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="0958f-109">語法</span><span class="sxs-lookup"><span data-stu-id="0958f-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0958f-110">參數</span><span class="sxs-lookup"><span data-stu-id="0958f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0958f-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="0958f-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="0958f-113">值</span><span class="sxs-lookup"><span data-stu-id="0958f-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="0958f-114">意義</span><span class="sxs-lookup"><span data-stu-id="0958f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="0958f-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0958f-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="0958f-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="0958f-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="0958f-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0958f-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0958f-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="0958f-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0958f-119">*pItemType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-120">GUID 的指標，識別要開啟之專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="0958f-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="0958f-121">*pItemSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-122">GUID 的指標，指出要開啟的專案子類型。</span><span class="sxs-lookup"><span data-stu-id="0958f-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="0958f-123">*szItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-124">字串，包含要開啟之專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="0958f-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="0958f-125">*ModeFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-126">描述指定的一組存取子句所適用的存取模式。</span><span class="sxs-lookup"><span data-stu-id="0958f-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="0958f-127">如需詳細資訊，請參閱 [**PStore 類型**](pstore-types.md)。</span><span class="sxs-lookup"><span data-stu-id="0958f-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="0958f-128">值</span><span class="sxs-lookup"><span data-stu-id="0958f-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="0958f-129">意義</span><span class="sxs-lookup"><span data-stu-id="0958f-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="0958f-130"><dt>**PST \_讀取**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="0958f-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="0958f-131">讀取存取模式。</span><span class="sxs-lookup"><span data-stu-id="0958f-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="0958f-132"><dt>**PST \_寫入**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="0958f-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="0958f-133">寫入存取模式。</span><span class="sxs-lookup"><span data-stu-id="0958f-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0958f-134">*pProomptInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-135">[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0958f-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0958f-136">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0958f-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0958f-137">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="0958f-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0958f-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="0958f-138">Return value</span></span>

<span data-ttu-id="0958f-139">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0958f-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="0958f-140">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="0958f-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0958f-141">備註</span><span class="sxs-lookup"><span data-stu-id="0958f-141">Remarks</span></span>

<span data-ttu-id="0958f-142">使用 **OpenItem** 在受保護的儲存體資料庫中開啟專案時，需要最後使用 [**IPStore：： CloseItem**](ipstore-closeitem.md) 來關閉專案，以避免記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="0958f-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="0958f-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="0958f-143">Requirements</span></span>



| <span data-ttu-id="0958f-144">需求</span><span class="sxs-lookup"><span data-stu-id="0958f-144">Requirement</span></span> | <span data-ttu-id="0958f-145">值</span><span class="sxs-lookup"><span data-stu-id="0958f-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0958f-146">標頭</span><span class="sxs-lookup"><span data-stu-id="0958f-146">Header</span></span><br/> | <dl> <span data-ttu-id="0958f-147"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="0958f-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0958f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0958f-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="0958f-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0958f-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0958f-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0958f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0958f-151">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="0958f-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="0958f-152">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="0958f-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
