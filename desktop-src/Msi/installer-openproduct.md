---
description: 安裝程式物件的 OpenProduct 方法會使用產品代碼開啟已安裝產品的安裝程式套件，並傳回會話物件。
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: OpenProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991344"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="8be71-103">OpenProduct 方法</span><span class="sxs-lookup"><span data-stu-id="8be71-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="8be71-104">[**安裝程式**](installer-object.md)物件的 **OpenProduct** 方法會使用產品代碼開啟已安裝產品的安裝程式套件，並傳回 [**會話**](session-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="8be71-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be71-105">語法</span><span class="sxs-lookup"><span data-stu-id="8be71-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="8be71-106">參數</span><span class="sxs-lookup"><span data-stu-id="8be71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be71-107">*productCode*</span><span class="sxs-lookup"><span data-stu-id="8be71-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="8be71-108">必要的字串，其中包含唯一的產品代碼 ([GUID](guid.md)) 或安裝程式所寫入的啟用描述項。</span><span class="sxs-lookup"><span data-stu-id="8be71-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be71-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8be71-109">Return value</span></span>

<span data-ttu-id="8be71-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8be71-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be71-111">備註</span><span class="sxs-lookup"><span data-stu-id="8be71-111">Remarks</span></span>

<span data-ttu-id="8be71-112">請注意，單一進程只能開啟一個 [**會話**](session-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8be71-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="8be71-113">**OpenProduct** 不能用在自訂動作中，因為使用中的安裝是唯一允許的會話。</span><span class="sxs-lookup"><span data-stu-id="8be71-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be71-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8be71-114">Requirements</span></span>



| <span data-ttu-id="8be71-115">需求</span><span class="sxs-lookup"><span data-stu-id="8be71-115">Requirement</span></span> | <span data-ttu-id="8be71-116">值</span><span class="sxs-lookup"><span data-stu-id="8be71-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be71-117">版本</span><span class="sxs-lookup"><span data-stu-id="8be71-117">Version</span></span><br/> | <span data-ttu-id="8be71-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8be71-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8be71-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8be71-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8be71-120">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8be71-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8be71-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8be71-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8be71-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be71-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8be71-123">IID</span><span class="sxs-lookup"><span data-stu-id="8be71-123">IID</span></span><br/>     | <span data-ttu-id="8be71-124">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8be71-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




