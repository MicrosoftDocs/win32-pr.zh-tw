---
description: 安裝程式物件的 CreateRecord 方法會傳回具有所要求欄位數目的新記錄物件。
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: CreateRecord 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991261"
---
# <a name="installercreaterecord-method"></a><span data-ttu-id="8cefa-103">CreateRecord 方法</span><span class="sxs-lookup"><span data-stu-id="8cefa-103">Installer.CreateRecord method</span></span>

<span data-ttu-id="8cefa-104">[**安裝程式**](installer-object.md)物件的 **CreateRecord** 方法會傳回具有所要求欄位數目的新 [**記錄**](record-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="8cefa-104">The **CreateRecord** method of the [**Installer**](installer-object.md) object returns a new [**Record**](record-object.md) object with the requested number of fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cefa-105">語法</span><span class="sxs-lookup"><span data-stu-id="8cefa-105">Syntax</span></span>


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a><span data-ttu-id="8cefa-106">參數</span><span class="sxs-lookup"><span data-stu-id="8cefa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cefa-107">*計數*</span><span class="sxs-lookup"><span data-stu-id="8cefa-107">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="8cefa-108">需要的欄位數目，可能是0。</span><span class="sxs-lookup"><span data-stu-id="8cefa-108">Required number of fields, which may be 0.</span></span> <span data-ttu-id="8cefa-109">記錄中欄位的最大數目限制為65535。</span><span class="sxs-lookup"><span data-stu-id="8cefa-109">The maximum number of fields in a record is limited to 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cefa-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cefa-110">Return value</span></span>

<span data-ttu-id="8cefa-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8cefa-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cefa-112">備註</span><span class="sxs-lookup"><span data-stu-id="8cefa-112">Remarks</span></span>

<span data-ttu-id="8cefa-113">欄位0（而不是 *計數* 中的其中一個欄位）通常用於記錄導向的專案，例如格式字串或執行 op 程式碼。</span><span class="sxs-lookup"><span data-stu-id="8cefa-113">Field 0, not one of the fields in *count*, is normally used for record-oriented items such as format strings or execution op-codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cefa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cefa-114">Requirements</span></span>



| <span data-ttu-id="8cefa-115">需求</span><span class="sxs-lookup"><span data-stu-id="8cefa-115">Requirement</span></span> | <span data-ttu-id="8cefa-116">值</span><span class="sxs-lookup"><span data-stu-id="8cefa-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cefa-117">版本</span><span class="sxs-lookup"><span data-stu-id="8cefa-117">Version</span></span><br/> | <span data-ttu-id="8cefa-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8cefa-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8cefa-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8cefa-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8cefa-120">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8cefa-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8cefa-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8cefa-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8cefa-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cefa-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8cefa-123">IID</span><span class="sxs-lookup"><span data-stu-id="8cefa-123">IID</span></span><br/>     | <span data-ttu-id="8cefa-124">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8cefa-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




