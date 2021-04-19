---
description: 建立 MP3 媒體來源的位元組資料流程處理常式。
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974143"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="c378f-103">MFCreateMP3ByteStreamPlugin 函式</span><span class="sxs-lookup"><span data-stu-id="c378f-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="c378f-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c378f-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="c378f-105">相反地，應用程式應該使用 [來源解析](source-resolver.md) 程式來建立 MP3 媒體來源。\]</span><span class="sxs-lookup"><span data-stu-id="c378f-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="c378f-106">建立 MP3 媒體來源的位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="c378f-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="c378f-107">語法</span><span class="sxs-lookup"><span data-stu-id="c378f-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="c378f-108">參數</span><span class="sxs-lookup"><span data-stu-id="c378f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c378f-109">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c378f-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c378f-110">所要求介面的介面識別項 (IID)。</span><span class="sxs-lookup"><span data-stu-id="c378f-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="c378f-111">將此參數設定為 **IID \_ IMFByteStreamHandler** ，以接收 [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c378f-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c378f-112">*ppvHandler* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c378f-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c378f-113">接收介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c378f-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="c378f-114">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="c378f-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c378f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c378f-115">Return value</span></span>

<span data-ttu-id="c378f-116">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c378f-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c378f-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c378f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c378f-118">備註</span><span class="sxs-lookup"><span data-stu-id="c378f-118">Remarks</span></span>

<span data-ttu-id="c378f-119">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="c378f-119">This function has no associated import library.</span></span> <span data-ttu-id="c378f-120">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 mf.dll。</span><span class="sxs-lookup"><span data-stu-id="c378f-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c378f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c378f-121">Requirements</span></span>



| <span data-ttu-id="c378f-122">需求</span><span class="sxs-lookup"><span data-stu-id="c378f-122">Requirement</span></span> | <span data-ttu-id="c378f-123">值</span><span class="sxs-lookup"><span data-stu-id="c378f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c378f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c378f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c378f-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c378f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c378f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c378f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c378f-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c378f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c378f-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c378f-128">End of client support</span></span><br/>    | <span data-ttu-id="c378f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c378f-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="c378f-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c378f-130">End of server support</span></span><br/>    | <span data-ttu-id="c378f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c378f-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c378f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c378f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c378f-133">媒體基礎函式</span><span class="sxs-lookup"><span data-stu-id="c378f-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="c378f-134">配置處理常式和 Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="c378f-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="c378f-135">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="c378f-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
