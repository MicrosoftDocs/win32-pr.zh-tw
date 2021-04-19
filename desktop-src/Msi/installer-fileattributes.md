---
description: 安裝程式物件的 FileAttributes 屬性會傳回數位，表示檔案或資料夾之指定路徑的合併檔案屬性。
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: 'FileAttributes 屬性 (Windows. .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988258"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="b8224-103">FileAttributes 屬性</span><span class="sxs-lookup"><span data-stu-id="b8224-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="b8224-104">[**安裝程式**](installer-object.md)物件的 **FileAttributes** 屬性會傳回數位，表示檔案或資料夾之指定路徑的合併檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="b8224-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="b8224-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b8224-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8224-106">語法</span><span class="sxs-lookup"><span data-stu-id="b8224-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="b8224-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="b8224-107">Property value</span></span>

<span data-ttu-id="b8224-108">檔案或資料夾的必要路徑。</span><span class="sxs-lookup"><span data-stu-id="b8224-108">The required path to the file or folder.</span></span> <span data-ttu-id="b8224-109">部分路徑會假設目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="b8224-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8224-110">備註</span><span class="sxs-lookup"><span data-stu-id="b8224-110">Remarks</span></span>

<span data-ttu-id="b8224-111">**FileAttributes** 屬性會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="b8224-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="b8224-112">檔案屬性</span><span class="sxs-lookup"><span data-stu-id="b8224-112">File attribute</span></span>              | <span data-ttu-id="b8224-113">值</span><span class="sxs-lookup"><span data-stu-id="b8224-113">Value</span></span>      | <span data-ttu-id="b8224-114">值</span><span class="sxs-lookup"><span data-stu-id="b8224-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="b8224-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="b8224-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="b8224-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b8224-116">0x00000001</span></span> | <span data-ttu-id="b8224-117">1</span><span class="sxs-lookup"><span data-stu-id="b8224-117">1</span></span>     |
| <span data-ttu-id="b8224-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="b8224-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="b8224-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b8224-119">0x00000002</span></span> | <span data-ttu-id="b8224-120">2</span><span class="sxs-lookup"><span data-stu-id="b8224-120">2</span></span>     |
| <span data-ttu-id="b8224-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="b8224-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="b8224-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b8224-122">0x00000004</span></span> | <span data-ttu-id="b8224-123">4</span><span class="sxs-lookup"><span data-stu-id="b8224-123">4</span></span>     |
| <span data-ttu-id="b8224-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="b8224-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="b8224-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8224-125">0x00000010</span></span> | <span data-ttu-id="b8224-126">16</span><span class="sxs-lookup"><span data-stu-id="b8224-126">16</span></span>    |
| <span data-ttu-id="b8224-127">檔 \_ 屬性 \_ 暫存</span><span class="sxs-lookup"><span data-stu-id="b8224-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="b8224-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="b8224-128">0x00000100</span></span> | <span data-ttu-id="b8224-129">256</span><span class="sxs-lookup"><span data-stu-id="b8224-129">256</span></span>   |
| <span data-ttu-id="b8224-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="b8224-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="b8224-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="b8224-131">0x00000800</span></span> | <span data-ttu-id="b8224-132">2048</span><span class="sxs-lookup"><span data-stu-id="b8224-132">2048</span></span>  |
| <span data-ttu-id="b8224-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b8224-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="b8224-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="b8224-134">0x00001000</span></span> | <span data-ttu-id="b8224-135">4096</span><span class="sxs-lookup"><span data-stu-id="b8224-135">4096</span></span>  |



 

<span data-ttu-id="b8224-136">如果檔案或資料夾不存在或無法存取，則會傳回–1。</span><span class="sxs-lookup"><span data-stu-id="b8224-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8224-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8224-137">Requirements</span></span>



| <span data-ttu-id="b8224-138">需求</span><span class="sxs-lookup"><span data-stu-id="b8224-138">Requirement</span></span> | <span data-ttu-id="b8224-139">值</span><span class="sxs-lookup"><span data-stu-id="b8224-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8224-140">版本</span><span class="sxs-lookup"><span data-stu-id="b8224-140">Version</span></span><br/> | <span data-ttu-id="b8224-141">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b8224-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b8224-142">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b8224-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b8224-143">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b8224-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b8224-144">標頭</span><span class="sxs-lookup"><span data-stu-id="b8224-144">Header</span></span><br/>  | <dl> <span data-ttu-id="b8224-145"><dt>：。H</dt></span><span class="sxs-lookup"><span data-stu-id="b8224-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="b8224-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b8224-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8224-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8224-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b8224-148">IID</span><span class="sxs-lookup"><span data-stu-id="b8224-148">IID</span></span><br/>     | <span data-ttu-id="b8224-149">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b8224-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




