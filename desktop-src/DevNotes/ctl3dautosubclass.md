---
description: 自動子類別，並將3D 效果加入至應用程式中的所有對話方塊。
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979465"
---
# <a name="ctl3dautosubclass-function"></a><span data-ttu-id="15273-103">Ctl3dAutoSubclass 函式</span><span class="sxs-lookup"><span data-stu-id="15273-103">Ctl3dAutoSubclass function</span></span>

<span data-ttu-id="15273-104">自動子類別，並將3D 效果加入至應用程式中的所有對話方塊。</span><span class="sxs-lookup"><span data-stu-id="15273-104">Automatically subclasses and adds 3D effects to all dialog boxes in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="15273-105">語法</span><span class="sxs-lookup"><span data-stu-id="15273-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="15273-106">參數</span><span class="sxs-lookup"><span data-stu-id="15273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15273-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="15273-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="15273-108">要註冊為用戶端之應用程式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="15273-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15273-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="15273-109">Return value</span></span>

<span data-ttu-id="15273-110">除非下列其中一個條件存在，否則會傳回 **TRUE** ，在此情況下，它會傳回 **FALSE**：</span><span class="sxs-lookup"><span data-stu-id="15273-110">Returns **TRUE** unless one of the following conditions exists, in which case it returns **FALSE**:</span></span>

-   <span data-ttu-id="15273-111">CTL3D 正在 Windows 3.0 版或更早版本下執行。</span><span class="sxs-lookup"><span data-stu-id="15273-111">CTL3D is running under Windows version 3.0 or earlier.</span></span>
-   <span data-ttu-id="15273-112">CTL3D 目前的應用程式在其資料表中沒有可用的空間。</span><span class="sxs-lookup"><span data-stu-id="15273-112">CTL3D does not have space available in its tables for the current application.</span></span> <span data-ttu-id="15273-113">CTL3D 可同時服務多達32的應用程式。</span><span class="sxs-lookup"><span data-stu-id="15273-113">CTL3D can service up to 32 applications at the same time.</span></span>
-   <span data-ttu-id="15273-114">CTL3D 無法安裝其 CBT 勾點。</span><span class="sxs-lookup"><span data-stu-id="15273-114">CTL3D cannot install its CBT hook.</span></span>

## <a name="remarks"></a><span data-ttu-id="15273-115">備註</span><span class="sxs-lookup"><span data-stu-id="15273-115">Remarks</span></span>

<span data-ttu-id="15273-116">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="15273-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="15273-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="15273-117">Requirements</span></span>



| <span data-ttu-id="15273-118">需求</span><span class="sxs-lookup"><span data-stu-id="15273-118">Requirement</span></span> | <span data-ttu-id="15273-119">值</span><span class="sxs-lookup"><span data-stu-id="15273-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15273-120">DLL</span><span class="sxs-lookup"><span data-stu-id="15273-120">DLL</span></span><br/> | <dl> <span data-ttu-id="15273-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15273-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
