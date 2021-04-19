---
description: 提供 COM 標準方法來管理受保護的儲存資料項目。
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: 'IPStore 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992792"
---
# <a name="ipstore-interface"></a><span data-ttu-id="2483d-103">IPStore 介面</span><span class="sxs-lookup"><span data-stu-id="2483d-103">IPStore interface</span></span>

<span data-ttu-id="2483d-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2483d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2483d-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="2483d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2483d-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="2483d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2483d-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="2483d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2483d-108">\[這個介面可能會在未來的 Windows 版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2483d-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="2483d-109">提供 COM 標準方法來管理受保護的儲存資料項目。</span><span class="sxs-lookup"><span data-stu-id="2483d-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="2483d-110">[**PStoreCreateInstance**](pstorecreateinstance.md)方法會傳回這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2483d-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="2483d-111">成員</span><span class="sxs-lookup"><span data-stu-id="2483d-111">Members</span></span>

<span data-ttu-id="2483d-112">**IPStore** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2483d-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2483d-113">**IPStore** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2483d-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="2483d-114">方法</span><span class="sxs-lookup"><span data-stu-id="2483d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2483d-115">方法</span><span class="sxs-lookup"><span data-stu-id="2483d-115">Methods</span></span>

<span data-ttu-id="2483d-116">**IPStore** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2483d-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="2483d-117">方法</span><span class="sxs-lookup"><span data-stu-id="2483d-117">Method</span></span>                                                   | <span data-ttu-id="2483d-118">描述</span><span class="sxs-lookup"><span data-stu-id="2483d-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2483d-119">**CloseItem**</span><span class="sxs-lookup"><span data-stu-id="2483d-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="2483d-120">從受保護的儲存體關閉指定的資料項目。</span><span class="sxs-lookup"><span data-stu-id="2483d-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="2483d-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="2483d-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="2483d-122">在指定的型別內建立指定的子類型。</span><span class="sxs-lookup"><span data-stu-id="2483d-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="2483d-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="2483d-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="2483d-124">使用指定的名稱建立指定的型別。</span><span class="sxs-lookup"><span data-stu-id="2483d-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="2483d-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="2483d-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="2483d-126">從受保護的儲存體中刪除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="2483d-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="2483d-127">**DeleteSubtype**</span><span class="sxs-lookup"><span data-stu-id="2483d-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="2483d-128">從受保護的儲存體中刪除指定的專案子類型。</span><span class="sxs-lookup"><span data-stu-id="2483d-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="2483d-129">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="2483d-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="2483d-130">從受保護的儲存體中刪除指定的類型。</span><span class="sxs-lookup"><span data-stu-id="2483d-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="2483d-131">**EnumItems**</span><span class="sxs-lookup"><span data-stu-id="2483d-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="2483d-132">傳回用來列舉受保護儲存資料庫中專案的子類型介面指標。</span><span class="sxs-lookup"><span data-stu-id="2483d-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="2483d-133">**EnumSubtypes**</span><span class="sxs-lookup"><span data-stu-id="2483d-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="2483d-134">傳回介面，以列舉受保護資料庫中目前註冊之類型的子類型。</span><span class="sxs-lookup"><span data-stu-id="2483d-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="2483d-135">**EnumTypes**</span><span class="sxs-lookup"><span data-stu-id="2483d-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="2483d-136">傳回介面，以列舉受保護資料庫中目前註冊的類型。</span><span class="sxs-lookup"><span data-stu-id="2483d-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="2483d-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="2483d-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="2483d-138">抓取儲存提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2483d-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="2483d-139">**GetProvParam**</span><span class="sxs-lookup"><span data-stu-id="2483d-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="2483d-140">未實作。</span><span class="sxs-lookup"><span data-stu-id="2483d-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2483d-141">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="2483d-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="2483d-142">捕獲與子類型相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="2483d-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="2483d-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="2483d-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="2483d-144">抓取與類型相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="2483d-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="2483d-145">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="2483d-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="2483d-146">開啟多個存取的專案。</span><span class="sxs-lookup"><span data-stu-id="2483d-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="2483d-147">**ReadAccessRuleSet**</span><span class="sxs-lookup"><span data-stu-id="2483d-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="2483d-148">未實作。</span><span class="sxs-lookup"><span data-stu-id="2483d-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2483d-149">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="2483d-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="2483d-150">從受保護的儲存體讀取指定的資料項目。</span><span class="sxs-lookup"><span data-stu-id="2483d-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="2483d-151">**SetProvParam**</span><span class="sxs-lookup"><span data-stu-id="2483d-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="2483d-152">設定指定的參數資訊。</span><span class="sxs-lookup"><span data-stu-id="2483d-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="2483d-153">**WriteAccessRuleset**</span><span class="sxs-lookup"><span data-stu-id="2483d-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="2483d-154">未實作。</span><span class="sxs-lookup"><span data-stu-id="2483d-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2483d-155">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="2483d-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="2483d-156">將資料項目寫入受保護的儲存體。</span><span class="sxs-lookup"><span data-stu-id="2483d-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="2483d-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="2483d-157">Requirements</span></span>



| <span data-ttu-id="2483d-158">需求</span><span class="sxs-lookup"><span data-stu-id="2483d-158">Requirement</span></span> | <span data-ttu-id="2483d-159">值</span><span class="sxs-lookup"><span data-stu-id="2483d-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2483d-160">標頭</span><span class="sxs-lookup"><span data-stu-id="2483d-160">Header</span></span><br/> | <dl> <span data-ttu-id="2483d-161"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="2483d-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2483d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="2483d-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="2483d-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2483d-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
