---
description: 安裝程式物件的 CollectUserInfo 方法會叫用使用者介面 wizard 順序，以收集並儲存使用者資訊和產品代碼。
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: CollectUserInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982645"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="aa8a0-103">CollectUserInfo 方法</span><span class="sxs-lookup"><span data-stu-id="aa8a0-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="aa8a0-104">[**安裝程式**](installer-object.md)物件的 **CollectUserInfo** 方法會叫用使用者介面 wizard 順序，以收集並儲存使用者資訊和產品代碼。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa8a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="aa8a0-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="aa8a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="aa8a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8a0-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="aa8a0-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8a0-108">指定產品的 [**產品代碼**](productcode.md) 。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa8a0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa8a0-109">Return value</span></span>

<span data-ttu-id="aa8a0-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa8a0-111">備註</span><span class="sxs-lookup"><span data-stu-id="aa8a0-111">Remarks</span></span>

<span data-ttu-id="aa8a0-112">應用程式在第一次執行時，應該呼叫 **CollectUserInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="aa8a0-113">**CollectUserInfo** 方法會開啟產品的安裝套件，並叫用可收集使用者資訊的撰寫使用者介面 wizard 順序。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="aa8a0-114">完成嚮導順序時，會註冊所收集的使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="aa8a0-115">[**UILevel**](installer-uilevel.md)屬性應該設定為 msiUILevelFull，因為此 API 需要撰寫的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="aa8a0-116">**CollectUserInfo** 方法會叫用 [ [firstrun.cmd] 對話方塊](firstrun-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8a0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa8a0-117">Requirements</span></span>



| <span data-ttu-id="aa8a0-118">需求</span><span class="sxs-lookup"><span data-stu-id="aa8a0-118">Requirement</span></span> | <span data-ttu-id="aa8a0-119">值</span><span class="sxs-lookup"><span data-stu-id="aa8a0-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8a0-120">版本</span><span class="sxs-lookup"><span data-stu-id="aa8a0-120">Version</span></span><br/> | <span data-ttu-id="aa8a0-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aa8a0-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="aa8a0-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aa8a0-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="aa8a0-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="aa8a0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aa8a0-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa8a0-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa8a0-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="aa8a0-126">IID</span><span class="sxs-lookup"><span data-stu-id="aa8a0-126">IID</span></span><br/>     | <span data-ttu-id="aa8a0-127">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="aa8a0-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="aa8a0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa8a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa8a0-129">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="aa8a0-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




