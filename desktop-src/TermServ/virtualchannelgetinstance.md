---
title: VirtualChannelGetInstance 進入點
description: 呼叫以讓外掛程式為 DLL 所執行的所有外掛程式建立 IWTSPlugin 介面的實例。
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- VirtualChannelGetInstance 進入點遠端桌面服務
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384270"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="340fa-104">VirtualChannelGetInstance 進入點</span><span class="sxs-lookup"><span data-stu-id="340fa-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="340fa-105">呼叫以讓外掛程式為 DLL 所執行的所有外掛程式建立 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="340fa-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="340fa-106">這個函式是由外掛程式所執行，而且必須依名稱匯出，讓應用程式可以使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至函數。</span><span class="sxs-lookup"><span data-stu-id="340fa-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="340fa-107">這個函式的原型不包含在任何公用標頭檔中，因此您必須如所示明確地宣告它。</span><span class="sxs-lookup"><span data-stu-id="340fa-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="340fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="340fa-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="340fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="340fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="340fa-110">*refiid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="340fa-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="340fa-111">指定要傳回的介面類別型。</span><span class="sxs-lookup"><span data-stu-id="340fa-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="340fa-112">這必須是 **IID \_ IWTSPlugin**。</span><span class="sxs-lookup"><span data-stu-id="340fa-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="340fa-113">*pNumObjs* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="340fa-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="340fa-114">會接收所抓取介面數目的 **ULONG** 變數位址。</span><span class="sxs-lookup"><span data-stu-id="340fa-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="340fa-115">*ppObjArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="340fa-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="340fa-116">接收介面指標之指標陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="340fa-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="340fa-117">如果這個參數是 **Null**，則實值必須將 DLL 所執行的外掛程式數目放在 *pNumObjs* 參數中。</span><span class="sxs-lookup"><span data-stu-id="340fa-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="340fa-118">這可讓呼叫端為 *ppObjArray* 配置適當的大小陣列。</span><span class="sxs-lookup"><span data-stu-id="340fa-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="340fa-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="340fa-119">Return value</span></span>

<span data-ttu-id="340fa-120">如果這個進入點成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="340fa-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="340fa-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="340fa-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="340fa-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="340fa-122">Requirements</span></span>



| <span data-ttu-id="340fa-123">需求</span><span class="sxs-lookup"><span data-stu-id="340fa-123">Requirement</span></span> | <span data-ttu-id="340fa-124">值</span><span class="sxs-lookup"><span data-stu-id="340fa-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="340fa-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="340fa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="340fa-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="340fa-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="340fa-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="340fa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="340fa-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="340fa-128">Windows Server 2008</span></span><br/> |



 

