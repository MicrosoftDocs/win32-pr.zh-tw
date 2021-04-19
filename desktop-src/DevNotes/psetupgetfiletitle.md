---
description: 抓取指定檔案路徑的檔案標題。
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: pSetupGetFileTitle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975967"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="72f60-103">pSetupGetFileTitle 函式</span><span class="sxs-lookup"><span data-stu-id="72f60-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="72f60-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="72f60-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="72f60-105">抓取指定檔案路徑的檔案標題。</span><span class="sxs-lookup"><span data-stu-id="72f60-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f60-106">語法</span><span class="sxs-lookup"><span data-stu-id="72f60-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="72f60-107">參數</span><span class="sxs-lookup"><span data-stu-id="72f60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f60-108">*FilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72f60-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f60-109">檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="72f60-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f60-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="72f60-110">Return value</span></span>

<span data-ttu-id="72f60-111">接收檔案標題之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="72f60-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f60-112">備註</span><span class="sxs-lookup"><span data-stu-id="72f60-112">Remarks</span></span>

<span data-ttu-id="72f60-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="72f60-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f60-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="72f60-114">Requirements</span></span>



| <span data-ttu-id="72f60-115">需求</span><span class="sxs-lookup"><span data-stu-id="72f60-115">Requirement</span></span> | <span data-ttu-id="72f60-116">值</span><span class="sxs-lookup"><span data-stu-id="72f60-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72f60-117">DLL</span><span class="sxs-lookup"><span data-stu-id="72f60-117">DLL</span></span><br/> | <dl> <span data-ttu-id="72f60-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f60-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
