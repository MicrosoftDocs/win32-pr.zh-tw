---
description: 在提供 Jet 錯誤時， (IDA) 和未格式化的訊息字串，抓取錯誤碼識別碼。
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975956"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="5426d-103">JetErrRawMessage 函式</span><span class="sxs-lookup"><span data-stu-id="5426d-103">JetErrRawMessage function</span></span>

<span data-ttu-id="5426d-104">在提供 Jet 錯誤時， (IDA) 和未格式化的訊息字串，抓取錯誤碼識別碼。</span><span class="sxs-lookup"><span data-stu-id="5426d-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="5426d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5426d-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="5426d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5426d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5426d-107">*犯 錯*</span><span class="sxs-lookup"><span data-stu-id="5426d-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-108">與所取得資訊對應的 Jet 錯誤。</span><span class="sxs-lookup"><span data-stu-id="5426d-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="5426d-109">*pIda*</span><span class="sxs-lookup"><span data-stu-id="5426d-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-110">IDA 的指標。</span><span class="sxs-lookup"><span data-stu-id="5426d-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="5426d-111">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="5426d-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-112">錯誤訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="5426d-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="5426d-113">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="5426d-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-114">錯誤訊息中的位元組數目計數。</span><span class="sxs-lookup"><span data-stu-id="5426d-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="5426d-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="5426d-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-116">讀取的實際位元組數目的指標。</span><span class="sxs-lookup"><span data-stu-id="5426d-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="5426d-117">*pCoNtextId*</span><span class="sxs-lookup"><span data-stu-id="5426d-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-118">與說明檔相關聯之內容識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="5426d-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="5426d-119">*pwszHelp/file*</span><span class="sxs-lookup"><span data-stu-id="5426d-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="5426d-120">指向說明錯誤之檔案的指標。</span><span class="sxs-lookup"><span data-stu-id="5426d-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5426d-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="5426d-121">Return value</span></span>

<span data-ttu-id="5426d-122">如果函式成功，它會傳回 **JET \_ errSuccess**，否則會傳回未格式化的錯誤訊息，指出失敗的特定原因。</span><span class="sxs-lookup"><span data-stu-id="5426d-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5426d-123">備註</span><span class="sxs-lookup"><span data-stu-id="5426d-123">Remarks</span></span>

<span data-ttu-id="5426d-124">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5426d-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5426d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5426d-125">Requirements</span></span>



| <span data-ttu-id="5426d-126">需求</span><span class="sxs-lookup"><span data-stu-id="5426d-126">Requirement</span></span> | <span data-ttu-id="5426d-127">值</span><span class="sxs-lookup"><span data-stu-id="5426d-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5426d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5426d-128">DLL</span></span><br/> | <dl> <span data-ttu-id="5426d-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5426d-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
