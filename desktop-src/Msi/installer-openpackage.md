---
description: 安裝程式物件的 OpenPackage 方法會開啟安裝程式封裝，以搭配存取產品資料庫和安裝引擎的函式使用，以傳回會話物件。
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: OpenPackage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989260"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="90be4-103">OpenPackage 方法</span><span class="sxs-lookup"><span data-stu-id="90be4-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="90be4-104">[**安裝程式**](installer-object.md)物件的 **OpenPackage** 方法會開啟安裝程式封裝，以搭配存取產品資料庫和安裝引擎的函式使用，以傳回 [**會話**](session-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="90be4-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="90be4-105">語法</span><span class="sxs-lookup"><span data-stu-id="90be4-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="90be4-106">參數</span><span class="sxs-lookup"><span data-stu-id="90be4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90be4-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="90be4-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="90be4-108">必要的字串，其中包含封裝的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="90be4-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="90be4-109">*options*</span><span class="sxs-lookup"><span data-stu-id="90be4-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="90be4-110">選擇性的整數值，指定當建立會話物件時， **OpenPackage** 是否應該忽略目前的電腦狀態。</span><span class="sxs-lookup"><span data-stu-id="90be4-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="90be4-111">如果選項預設為原始行為，則沒有值或0值。</span><span class="sxs-lookup"><span data-stu-id="90be4-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="90be4-112">當選項為1時， **OpenPackage** 方法會在開啟封裝時忽略目前的電腦狀態。</span><span class="sxs-lookup"><span data-stu-id="90be4-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="90be4-113">值為1時，可防止變更目前的電腦狀態。</span><span class="sxs-lookup"><span data-stu-id="90be4-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="90be4-114">如需詳細資訊，請參閱 [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)。</span><span class="sxs-lookup"><span data-stu-id="90be4-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90be4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="90be4-115">Return value</span></span>

<span data-ttu-id="90be4-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="90be4-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90be4-117">備註</span><span class="sxs-lookup"><span data-stu-id="90be4-117">Remarks</span></span>

<span data-ttu-id="90be4-118">**OpenPackage** 方法可以直接接受資料庫控制碼，而不是封裝路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="90be4-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="90be4-119">請注意，單一進程只能開啟一個 [**會話**](session-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="90be4-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="90be4-120">**OpenPackage** 不能用在自訂動作中，因為使用中的安裝是唯一允許的會話。</span><span class="sxs-lookup"><span data-stu-id="90be4-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="90be4-121">安全 [**會話**](session-object.md) 物件會在開啟封裝時忽略目前的電腦狀態，並防止變更目前的電腦狀態。</span><span class="sxs-lookup"><span data-stu-id="90be4-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="90be4-122">如需詳細資訊，請參閱 [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)。</span><span class="sxs-lookup"><span data-stu-id="90be4-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="90be4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="90be4-123">Requirements</span></span>



| <span data-ttu-id="90be4-124">需求</span><span class="sxs-lookup"><span data-stu-id="90be4-124">Requirement</span></span> | <span data-ttu-id="90be4-125">值</span><span class="sxs-lookup"><span data-stu-id="90be4-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90be4-126">版本</span><span class="sxs-lookup"><span data-stu-id="90be4-126">Version</span></span><br/> | <span data-ttu-id="90be4-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="90be4-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="90be4-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="90be4-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="90be4-129">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="90be4-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="90be4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="90be4-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="90be4-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90be4-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="90be4-132">IID</span><span class="sxs-lookup"><span data-stu-id="90be4-132">IID</span></span><br/>     | <span data-ttu-id="90be4-133">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="90be4-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




