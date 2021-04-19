---
description: 指出目前正在執行的 CTL3D 版本。
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978462"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="18cb5-103">Ctl3dGetVer 函式</span><span class="sxs-lookup"><span data-stu-id="18cb5-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="18cb5-104">指出目前正在執行的 CTL3D 版本。</span><span class="sxs-lookup"><span data-stu-id="18cb5-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="18cb5-105">語法</span><span class="sxs-lookup"><span data-stu-id="18cb5-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="18cb5-106">參數</span><span class="sxs-lookup"><span data-stu-id="18cb5-106">Parameters</span></span>

<span data-ttu-id="18cb5-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="18cb5-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18cb5-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="18cb5-108">Return value</span></span>

<span data-ttu-id="18cb5-109">傳回值，其中包含高序位位元組的主要版本號碼，以及低序位位元組中的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="18cb5-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="18cb5-110">備註</span><span class="sxs-lookup"><span data-stu-id="18cb5-110">Remarks</span></span>

<span data-ttu-id="18cb5-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="18cb5-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="18cb5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="18cb5-112">Requirements</span></span>



| <span data-ttu-id="18cb5-113">需求</span><span class="sxs-lookup"><span data-stu-id="18cb5-113">Requirement</span></span> | <span data-ttu-id="18cb5-114">值</span><span class="sxs-lookup"><span data-stu-id="18cb5-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18cb5-115">DLL</span><span class="sxs-lookup"><span data-stu-id="18cb5-115">DLL</span></span><br/> | <dl> <span data-ttu-id="18cb5-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18cb5-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
