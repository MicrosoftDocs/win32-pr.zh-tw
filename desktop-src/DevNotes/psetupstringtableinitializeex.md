---
description: 初始化字串資料表。
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992809"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="bb01e-103">pSetupStringTableInitializeEx 函式</span><span class="sxs-lookup"><span data-stu-id="bb01e-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="bb01e-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="bb01e-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="bb01e-105">初始化字串資料表。</span><span class="sxs-lookup"><span data-stu-id="bb01e-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb01e-106">語法</span><span class="sxs-lookup"><span data-stu-id="bb01e-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="bb01e-107">參數</span><span class="sxs-lookup"><span data-stu-id="bb01e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb01e-108">*ExtraDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb01e-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb01e-109">額外資料物件的大小。</span><span class="sxs-lookup"><span data-stu-id="bb01e-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="bb01e-110">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb01e-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb01e-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="bb01e-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb01e-112">備註</span><span class="sxs-lookup"><span data-stu-id="bb01e-112">Remarks</span></span>

<span data-ttu-id="bb01e-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="bb01e-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb01e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb01e-114">Requirements</span></span>



| <span data-ttu-id="bb01e-115">需求</span><span class="sxs-lookup"><span data-stu-id="bb01e-115">Requirement</span></span> | <span data-ttu-id="bb01e-116">值</span><span class="sxs-lookup"><span data-stu-id="bb01e-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb01e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="bb01e-117">DLL</span></span><br/> | <dl> <span data-ttu-id="bb01e-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb01e-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
