---
description: 抓取 (IDA) 的錯誤碼識別碼，並在提供 Jet 錯誤和延伸的錯誤資訊時，建立最後的顯示字串。
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988261"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="40712-103">JetErrFormattedMessage 函式</span><span class="sxs-lookup"><span data-stu-id="40712-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="40712-104">抓取 (IDA) 的錯誤碼識別碼，並在提供 Jet 錯誤和延伸的錯誤資訊時，建立最後的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="40712-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="40712-105">語法</span><span class="sxs-lookup"><span data-stu-id="40712-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="40712-106">參數</span><span class="sxs-lookup"><span data-stu-id="40712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40712-107">*犯 錯*</span><span class="sxs-lookup"><span data-stu-id="40712-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-108">用來查閱和格式化可顯示錯誤訊息的 Jet 錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="40712-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="40712-109">*pExtendedErrorInfo*</span><span class="sxs-lookup"><span data-stu-id="40712-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-110">所有的 Jet 錯誤資訊，包括資料庫名稱、資料表名稱和任何次要錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="40712-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="40712-111">*pIda*</span><span class="sxs-lookup"><span data-stu-id="40712-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-112">與特定錯誤碼相關聯之 IDA 的指標。</span><span class="sxs-lookup"><span data-stu-id="40712-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="40712-113">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="40712-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-114">錯誤訊息的指標。</span><span class="sxs-lookup"><span data-stu-id="40712-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="40712-115">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="40712-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-116">錯誤訊息中的位元組數目計數。</span><span class="sxs-lookup"><span data-stu-id="40712-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="40712-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="40712-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-118">讀取的實際位元組數目的指標。</span><span class="sxs-lookup"><span data-stu-id="40712-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="40712-119">*pCoNtextId*</span><span class="sxs-lookup"><span data-stu-id="40712-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-120">與說明檔相關聯之內容識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="40712-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="40712-121">*pwszHelp/file*</span><span class="sxs-lookup"><span data-stu-id="40712-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="40712-122">說明錯誤之檔案指標的指標。</span><span class="sxs-lookup"><span data-stu-id="40712-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40712-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="40712-123">Return value</span></span>

<span data-ttu-id="40712-124">如果函式成功，它會傳回 **JET \_ errSuccess**，否則會傳回格式化的錯誤訊息，指出失敗的特定原因。</span><span class="sxs-lookup"><span data-stu-id="40712-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="40712-125">備註</span><span class="sxs-lookup"><span data-stu-id="40712-125">Remarks</span></span>

<span data-ttu-id="40712-126">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="40712-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="40712-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="40712-127">Requirements</span></span>



| <span data-ttu-id="40712-128">需求</span><span class="sxs-lookup"><span data-stu-id="40712-128">Requirement</span></span> | <span data-ttu-id="40712-129">值</span><span class="sxs-lookup"><span data-stu-id="40712-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40712-130">DLL</span><span class="sxs-lookup"><span data-stu-id="40712-130">DLL</span></span><br/> | <dl> <span data-ttu-id="40712-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40712-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
