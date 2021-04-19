---
description: Database 物件的 Export 方法會將指定之資料表的結構和資料複製到文字封存檔案。
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990580"
---
# <a name="databaseexport-method"></a><span data-ttu-id="d319d-103">Database. Export 方法</span><span class="sxs-lookup"><span data-stu-id="d319d-103">Database.Export method</span></span>

<span data-ttu-id="d319d-104">[**Database**](database-object.md)物件的 **Export** 方法會將指定之資料表的結構和資料複製到 [文字](text-archive-files.md)封存檔案。</span><span class="sxs-lookup"><span data-stu-id="d319d-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d319d-105">語法</span><span class="sxs-lookup"><span data-stu-id="d319d-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="d319d-106">參數</span><span class="sxs-lookup"><span data-stu-id="d319d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d319d-107">*table*</span><span class="sxs-lookup"><span data-stu-id="d319d-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="d319d-108">資料庫資料表的必要名稱。</span><span class="sxs-lookup"><span data-stu-id="d319d-108">Required name of the database table.</span></span> <span data-ttu-id="d319d-109">如果使用安裝程式資料庫，則區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d319d-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="d319d-110">*path*</span><span class="sxs-lookup"><span data-stu-id="d319d-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="d319d-111">必要的字串，也就是放置文字檔的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="d319d-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="d319d-112">*file*</span><span class="sxs-lookup"><span data-stu-id="d319d-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="d319d-113">要建立之檔案的必要名稱。</span><span class="sxs-lookup"><span data-stu-id="d319d-113">Required name of the file to be created.</span></span> <span data-ttu-id="d319d-114">這不包含資料夾，因為必須在 path 物件中設定。</span><span class="sxs-lookup"><span data-stu-id="d319d-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d319d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d319d-115">Return value</span></span>

<span data-ttu-id="d319d-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d319d-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d319d-117">備註</span><span class="sxs-lookup"><span data-stu-id="d319d-117">Remarks</span></span>

<span data-ttu-id="d319d-118">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="d319d-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d319d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d319d-119">Requirements</span></span>



| <span data-ttu-id="d319d-120">需求</span><span class="sxs-lookup"><span data-stu-id="d319d-120">Requirement</span></span> | <span data-ttu-id="d319d-121">值</span><span class="sxs-lookup"><span data-stu-id="d319d-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d319d-122">版本</span><span class="sxs-lookup"><span data-stu-id="d319d-122">Version</span></span><br/> | <span data-ttu-id="d319d-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d319d-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d319d-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d319d-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d319d-125">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d319d-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d319d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d319d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="d319d-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d319d-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d319d-128">IID</span><span class="sxs-lookup"><span data-stu-id="d319d-128">IID</span></span><br/>     | <span data-ttu-id="d319d-129">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d319d-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




