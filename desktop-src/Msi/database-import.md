---
description: 資料庫物件的 Import 方法會從文字封存檔匯入資料庫資料表，並卸載任何現有的資料表。
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989797"
---
# <a name="databaseimport-method"></a><span data-ttu-id="39bae-103">Database. Import 方法</span><span class="sxs-lookup"><span data-stu-id="39bae-103">Database.Import method</span></span>

<span data-ttu-id="39bae-104">[**資料庫**](database-object.md)物件的 **Import** 方法會從 [文字](text-archive-files.md)封存檔匯入資料庫資料表，並卸載任何現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="39bae-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bae-105">語法</span><span class="sxs-lookup"><span data-stu-id="39bae-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="39bae-106">參數</span><span class="sxs-lookup"><span data-stu-id="39bae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bae-107">*path*</span><span class="sxs-lookup"><span data-stu-id="39bae-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="39bae-108">存在文字檔的必要資料夾。</span><span class="sxs-lookup"><span data-stu-id="39bae-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="39bae-109">*file*</span><span class="sxs-lookup"><span data-stu-id="39bae-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="39bae-110">要匯入之檔案的必要名稱。</span><span class="sxs-lookup"><span data-stu-id="39bae-110">Required name of the file to be imported.</span></span> <span data-ttu-id="39bae-111">這不包含資料夾，因為必須在 path 物件中設定。</span><span class="sxs-lookup"><span data-stu-id="39bae-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="39bae-112">資料表名稱是在檔案中指定的。</span><span class="sxs-lookup"><span data-stu-id="39bae-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bae-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="39bae-113">Return value</span></span>

<span data-ttu-id="39bae-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="39bae-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bae-115">備註</span><span class="sxs-lookup"><span data-stu-id="39bae-115">Remarks</span></span>

<span data-ttu-id="39bae-116">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="39bae-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bae-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="39bae-117">Requirements</span></span>



| <span data-ttu-id="39bae-118">需求</span><span class="sxs-lookup"><span data-stu-id="39bae-118">Requirement</span></span> | <span data-ttu-id="39bae-119">值</span><span class="sxs-lookup"><span data-stu-id="39bae-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39bae-120">版本</span><span class="sxs-lookup"><span data-stu-id="39bae-120">Version</span></span><br/> | <span data-ttu-id="39bae-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="39bae-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="39bae-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="39bae-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="39bae-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="39bae-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="39bae-124">DLL</span><span class="sxs-lookup"><span data-stu-id="39bae-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="39bae-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39bae-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="39bae-126">IID</span><span class="sxs-lookup"><span data-stu-id="39bae-126">IID</span></span><br/>     | <span data-ttu-id="39bae-127">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="39bae-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="39bae-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39bae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bae-129">**資料庫**</span><span class="sxs-lookup"><span data-stu-id="39bae-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="39bae-130">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="39bae-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




