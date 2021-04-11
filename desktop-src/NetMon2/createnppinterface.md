---
description: CreateNPPInterface 函式會使用 finder 傳回的 BLOB 來建立應用程式可使用的 NPP。
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: 'CreateNPPInterface 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944523"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="a3e94-103">CreateNPPInterface 函式</span><span class="sxs-lookup"><span data-stu-id="a3e94-103">CreateNPPInterface function</span></span>

<span data-ttu-id="a3e94-104">**CreateNPPInterface** 函式會使用 finder 傳回的 BLOB 來建立應用程式可使用的 NPP。</span><span class="sxs-lookup"><span data-stu-id="a3e94-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e94-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3e94-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="a3e94-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3e94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e94-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3e94-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e94-108">從搜尋工具傳回之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a3e94-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="a3e94-109"> \[ 中的 iid\]</span><span class="sxs-lookup"><span data-stu-id="a3e94-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e94-110">您從 NPP 呼叫之介面的識別碼 (**IRTC** 或 **IDelaydC**，例如) 。</span><span class="sxs-lookup"><span data-stu-id="a3e94-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="a3e94-111">*ppvObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3e94-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e94-112">傳回所要求介面之指標的指標。</span><span class="sxs-lookup"><span data-stu-id="a3e94-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e94-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3e94-113">Return value</span></span>

<span data-ttu-id="a3e94-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="a3e94-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a3e94-115">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="a3e94-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e94-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e94-116">Requirements</span></span>



| <span data-ttu-id="a3e94-117">需求</span><span class="sxs-lookup"><span data-stu-id="a3e94-117">Requirement</span></span> | <span data-ttu-id="a3e94-118">值</span><span class="sxs-lookup"><span data-stu-id="a3e94-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e94-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3e94-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e94-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e94-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3e94-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3e94-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e94-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3e94-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3e94-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a3e94-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e94-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a3e94-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a3e94-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3e94-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3e94-126"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3e94-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3e94-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e94-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e94-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e94-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




