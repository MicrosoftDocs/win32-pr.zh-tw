---
description: 安裝程式物件的 FileVersion 方法會使用安裝程式預期在資料庫中找到它們的格式，傳回路徑中指定之路徑的版本字串或語言字串。
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: FileVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982505"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="80a4f-103">FileVersion 方法</span><span class="sxs-lookup"><span data-stu-id="80a4f-103">Installer.FileVersion method</span></span>

<span data-ttu-id="80a4f-104">[**安裝程式**](installer-object.md)物件的 **FileVersion** 方法會使用安裝程式預期在資料庫中找到它們的格式，*傳回路徑中* 指定之路徑的版本字串或語言字串。</span><span class="sxs-lookup"><span data-stu-id="80a4f-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="80a4f-105">針對版本，這是 " \# ... \# \# \# " 格式的字串。</span><span class="sxs-lookup"><span data-stu-id="80a4f-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="80a4f-106">針對語言，這是十進位語言識別項。</span><span class="sxs-lookup"><span data-stu-id="80a4f-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a4f-107">語法</span><span class="sxs-lookup"><span data-stu-id="80a4f-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="80a4f-108">參數</span><span class="sxs-lookup"><span data-stu-id="80a4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a4f-109">*路徑*</span><span class="sxs-lookup"><span data-stu-id="80a4f-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="80a4f-110">必要的字串，其中包含檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="80a4f-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="80a4f-111">*Language*</span><span class="sxs-lookup"><span data-stu-id="80a4f-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="80a4f-112">旗標，用於指定傳回的值是否為語言識別項或版本字串。</span><span class="sxs-lookup"><span data-stu-id="80a4f-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="80a4f-113">TRUE 會傳回語言，FALSE 會傳回版本。</span><span class="sxs-lookup"><span data-stu-id="80a4f-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="80a4f-114">這個參數是選擇性的，預設值是 FALSE。</span><span class="sxs-lookup"><span data-stu-id="80a4f-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a4f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="80a4f-115">Return value</span></span>

<span data-ttu-id="80a4f-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="80a4f-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="80a4f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="80a4f-117">Requirements</span></span>



| <span data-ttu-id="80a4f-118">需求</span><span class="sxs-lookup"><span data-stu-id="80a4f-118">Requirement</span></span> | <span data-ttu-id="80a4f-119">值</span><span class="sxs-lookup"><span data-stu-id="80a4f-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a4f-120">版本</span><span class="sxs-lookup"><span data-stu-id="80a4f-120">Version</span></span><br/> | <span data-ttu-id="80a4f-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="80a4f-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="80a4f-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="80a4f-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="80a4f-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="80a4f-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="80a4f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="80a4f-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="80a4f-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80a4f-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="80a4f-126">IID</span><span class="sxs-lookup"><span data-stu-id="80a4f-126">IID</span></span><br/>     | <span data-ttu-id="80a4f-127">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="80a4f-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




