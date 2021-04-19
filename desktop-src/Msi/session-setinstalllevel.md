---
description: Session 物件的 SetInstallLevel 方法會將目前安裝的安裝層級設定為指定的值，並重新計算功能資料表中所有功能的 [選取] 和 [已安裝] 狀態。
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: SetInstallLevel 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993241"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="e6c80-103">SetInstallLevel 方法</span><span class="sxs-lookup"><span data-stu-id="e6c80-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="e6c80-104">[**Session**](session-object.md)物件的 **SetInstallLevel** 方法會將目前安裝的安裝層級設定為指定的值，並重新計算功能資料表中所有功能的 [選取] 和 [已安裝] 狀態。</span><span class="sxs-lookup"><span data-stu-id="e6c80-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="e6c80-105">它也會根據新的層級，設定 [元件資料表](component-table.md) 中每個元件的動作狀態。</span><span class="sxs-lookup"><span data-stu-id="e6c80-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c80-106">語法</span><span class="sxs-lookup"><span data-stu-id="e6c80-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="e6c80-107">參數</span><span class="sxs-lookup"><span data-stu-id="e6c80-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c80-108">*installLevel*</span><span class="sxs-lookup"><span data-stu-id="e6c80-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c80-109">需要新的安裝層級。</span><span class="sxs-lookup"><span data-stu-id="e6c80-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c80-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6c80-110">Return value</span></span>

<span data-ttu-id="e6c80-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e6c80-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6c80-112">備註</span><span class="sxs-lookup"><span data-stu-id="e6c80-112">Remarks</span></span>

<span data-ttu-id="e6c80-113">在呼叫 **SetInstallLevel** 之前，必須先執行 [CostInitialize 動作](costinitialize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e6c80-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="e6c80-114">如果為 *installLevel* 參數傳遞0，則不會變更目前的安裝層級，但仍會根據目前的安裝層級更新所有功能。</span><span class="sxs-lookup"><span data-stu-id="e6c80-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="e6c80-115">例如，處理常式模組可以使用這項功能，在 UI 選取程式中的任何時間點，將所有選取範圍重設回其初始預設狀態。</span><span class="sxs-lookup"><span data-stu-id="e6c80-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="e6c80-116">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="e6c80-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c80-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6c80-117">Requirements</span></span>



| <span data-ttu-id="e6c80-118">需求</span><span class="sxs-lookup"><span data-stu-id="e6c80-118">Requirement</span></span> | <span data-ttu-id="e6c80-119">值</span><span class="sxs-lookup"><span data-stu-id="e6c80-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c80-120">版本</span><span class="sxs-lookup"><span data-stu-id="e6c80-120">Version</span></span><br/> | <span data-ttu-id="e6c80-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e6c80-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6c80-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e6c80-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6c80-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e6c80-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e6c80-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c80-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6c80-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c80-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e6c80-126">IID</span><span class="sxs-lookup"><span data-stu-id="e6c80-126">IID</span></span><br/>     | <span data-ttu-id="e6c80-127">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e6c80-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




