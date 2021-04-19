---
description: SourceListForceResolution 方法會清除最後使用的來源屬性。
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: SourceListForceResolution 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995219"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="cdc6f-103">SourceListForceResolution 方法</span><span class="sxs-lookup"><span data-stu-id="cdc6f-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="cdc6f-104">**SourceListForceResolution** 方法會清除最後使用的來源屬性。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="cdc6f-105">這會強制安裝程式在下次需要 patch 來源時，于來源清單中搜尋有效的 patch 來源。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="cdc6f-106">例如，安裝程式要求修補程式來源在修補程式的本機快取複本遺失時，執行安裝或重新安裝。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="cdc6f-107">這個方法會呼叫 [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc6f-108">語法</span><span class="sxs-lookup"><span data-stu-id="cdc6f-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="cdc6f-109">參數</span><span class="sxs-lookup"><span data-stu-id="cdc6f-109">Parameters</span></span>

<span data-ttu-id="cdc6f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdc6f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdc6f-111">Return value</span></span>

<span data-ttu-id="cdc6f-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc6f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdc6f-113">Requirements</span></span>



| <span data-ttu-id="cdc6f-114">需求</span><span class="sxs-lookup"><span data-stu-id="cdc6f-114">Requirement</span></span> | <span data-ttu-id="cdc6f-115">值</span><span class="sxs-lookup"><span data-stu-id="cdc6f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc6f-116">版本</span><span class="sxs-lookup"><span data-stu-id="cdc6f-116">Version</span></span><br/> | <span data-ttu-id="cdc6f-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cdc6f-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cdc6f-119">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cdc6f-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="cdc6f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cdc6f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="cdc6f-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdc6f-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="cdc6f-122">IID</span><span class="sxs-lookup"><span data-stu-id="cdc6f-122">IID</span></span><br/>     | <span data-ttu-id="cdc6f-123">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cdc6f-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="cdc6f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdc6f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc6f-125">**Patch**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="cdc6f-126">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="cdc6f-127">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="cdc6f-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




