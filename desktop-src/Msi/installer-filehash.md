---
description: 安裝程式物件的 Get-filehash 方法會取得檔案的路徑，並傳回該檔案的128位雜湊。 檔案雜湊資訊會以記錄物件的形式傳回。 整個128位檔案雜湊會傳回為 4 32 位 IntegerData 屬性欄位。
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Get-filehash 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986804"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="a2eef-105">Get-filehash 方法</span><span class="sxs-lookup"><span data-stu-id="a2eef-105">Installer.FileHash method</span></span>

<span data-ttu-id="a2eef-106">[**安裝程式物件**](installer-object.md)的 **get-filehash** 方法會取得檔案的路徑，並傳回該檔案的128位雜湊。</span><span class="sxs-lookup"><span data-stu-id="a2eef-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="a2eef-107">檔案雜湊資訊會以 [**記錄物件**](record-object.md)的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="a2eef-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="a2eef-108">整個128位檔案雜湊會傳回為 4 32 位 [**IntegerData**](record-integerdata.md) 屬性欄位。</span><span class="sxs-lookup"><span data-stu-id="a2eef-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="a2eef-109">在 [**記錄物件**](record-object.md)中傳回的值會對應至 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)所傳回之 [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo)結構的四個欄位。</span><span class="sxs-lookup"><span data-stu-id="a2eef-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="a2eef-110">四個欄位的編號在 [MsiFileHash 資料表](msifilehash-table.md)中是以1為基礎。</span><span class="sxs-lookup"><span data-stu-id="a2eef-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="a2eef-111">欄位1對應至 HashPart1 資料行。</span><span class="sxs-lookup"><span data-stu-id="a2eef-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="a2eef-112">欄位2對應于 HashPart2 資料行。</span><span class="sxs-lookup"><span data-stu-id="a2eef-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="a2eef-113">欄位3對應于 HashPart3 資料行。</span><span class="sxs-lookup"><span data-stu-id="a2eef-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="a2eef-114">欄位4對應于 HashPart4 資料行。</span><span class="sxs-lookup"><span data-stu-id="a2eef-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2eef-115">語法</span><span class="sxs-lookup"><span data-stu-id="a2eef-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="a2eef-116">參數</span><span class="sxs-lookup"><span data-stu-id="a2eef-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2eef-117">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="a2eef-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="a2eef-118">要雜湊處理之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a2eef-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="a2eef-119">*選項*</span><span class="sxs-lookup"><span data-stu-id="a2eef-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="a2eef-120">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="a2eef-120">Reserved for future use.</span></span>

<span data-ttu-id="a2eef-121">此參數的值必須是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="a2eef-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2eef-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2eef-122">Return value</span></span>

<span data-ttu-id="a2eef-123">如果成功，這個方法會傳回包含檔案雜湊的 [**記錄物件**](record-object.md) 。</span><span class="sxs-lookup"><span data-stu-id="a2eef-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2eef-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2eef-124">Requirements</span></span>



| <span data-ttu-id="a2eef-125">需求</span><span class="sxs-lookup"><span data-stu-id="a2eef-125">Requirement</span></span> | <span data-ttu-id="a2eef-126">值</span><span class="sxs-lookup"><span data-stu-id="a2eef-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eef-127">版本</span><span class="sxs-lookup"><span data-stu-id="a2eef-127">Version</span></span><br/> | <span data-ttu-id="a2eef-128">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a2eef-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a2eef-129">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a2eef-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a2eef-130">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a2eef-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a2eef-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a2eef-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="a2eef-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2eef-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a2eef-133">IID</span><span class="sxs-lookup"><span data-stu-id="a2eef-133">IID</span></span><br/>     | <span data-ttu-id="a2eef-134">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a2eef-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="a2eef-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2eef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2eef-136">預設檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="a2eef-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="a2eef-137">管理檔案大小和版本</span><span class="sxs-lookup"><span data-stu-id="a2eef-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="a2eef-138">MsiFileHash 資料表</span><span class="sxs-lookup"><span data-stu-id="a2eef-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="a2eef-139">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="a2eef-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




