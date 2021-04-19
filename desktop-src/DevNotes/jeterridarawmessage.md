---
description: 當提供 (IDA) 的錯誤碼識別碼時，會抓取未格式化的訊息字串。
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997737"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="858f8-103">JetErrIDARawMessage 函式</span><span class="sxs-lookup"><span data-stu-id="858f8-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="858f8-104">當提供 (IDA) 的錯誤碼識別碼時，會抓取未格式化的訊息字串。</span><span class="sxs-lookup"><span data-stu-id="858f8-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="858f8-105">語法</span><span class="sxs-lookup"><span data-stu-id="858f8-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="858f8-106">參數</span><span class="sxs-lookup"><span data-stu-id="858f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="858f8-107">*艾達*</span><span class="sxs-lookup"><span data-stu-id="858f8-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="858f8-108">對應至特定錯誤碼的數位，並向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="858f8-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="858f8-109">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="858f8-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="858f8-110">錯誤訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="858f8-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="858f8-111">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="858f8-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="858f8-112">錯誤訊息中的位元組數目計數。</span><span class="sxs-lookup"><span data-stu-id="858f8-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="858f8-113">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="858f8-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="858f8-114">讀取的實際位元組數目的指標。</span><span class="sxs-lookup"><span data-stu-id="858f8-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="858f8-115">*pCoNtextId*</span><span class="sxs-lookup"><span data-stu-id="858f8-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="858f8-116">與說明檔相關聯之內容識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="858f8-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="858f8-117">*pwszHelp/file*</span><span class="sxs-lookup"><span data-stu-id="858f8-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="858f8-118">說明錯誤之檔案指標的指標。</span><span class="sxs-lookup"><span data-stu-id="858f8-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="858f8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="858f8-119">Return value</span></span>

<span data-ttu-id="858f8-120">如果函式成功，它會傳回 **JET \_ errSuccess**，否則會傳回未格式化的訊息，指出失敗的特定原因。</span><span class="sxs-lookup"><span data-stu-id="858f8-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="858f8-121">備註</span><span class="sxs-lookup"><span data-stu-id="858f8-121">Remarks</span></span>

<span data-ttu-id="858f8-122">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="858f8-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="858f8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="858f8-123">Requirements</span></span>



| <span data-ttu-id="858f8-124">需求</span><span class="sxs-lookup"><span data-stu-id="858f8-124">Requirement</span></span> | <span data-ttu-id="858f8-125">值</span><span class="sxs-lookup"><span data-stu-id="858f8-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="858f8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="858f8-126">DLL</span></span><br/> | <dl> <span data-ttu-id="858f8-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="858f8-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
