---
title: WMCreateStreamForURL 函式
description: WMCreateStreamForURL 函式是由應用程式所執行，以建立指定 URL 的 COM IStream 物件。
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- WMCreateStreamForURL 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373137"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="165b8-104">WMCreateStreamForURL 函式</span><span class="sxs-lookup"><span data-stu-id="165b8-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="165b8-105">**WMCreateStreamForURL** 函式是由應用程式所執行，以建立指定 URL 的 COM **IStream** 物件。</span><span class="sxs-lookup"><span data-stu-id="165b8-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="165b8-106">語法</span><span class="sxs-lookup"><span data-stu-id="165b8-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="165b8-107">參數</span><span class="sxs-lookup"><span data-stu-id="165b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165b8-108">*pwszURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="165b8-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="165b8-109">包含 URL 的寬字元字串的指標。</span><span class="sxs-lookup"><span data-stu-id="165b8-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="165b8-110">*pfCorrectSource* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="165b8-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="165b8-111">旗標的指標，true 將會防止 SDK 嘗試此 URL 的其他來源外掛程式。</span><span class="sxs-lookup"><span data-stu-id="165b8-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="165b8-112">*ppStream* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="165b8-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="165b8-113">方法所建立之 **IStream** 物件指標的指標。</span><span class="sxs-lookup"><span data-stu-id="165b8-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="165b8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="165b8-114">Return value</span></span>

<span data-ttu-id="165b8-115">如果函式成功，它必須傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="165b8-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="165b8-116">如果失敗，則必須傳回適當的 **HRESULT** 錯誤碼，而且 \* *PpStream* 應該設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="165b8-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="165b8-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="165b8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165b8-118">**來源外掛程式**</span><span class="sxs-lookup"><span data-stu-id="165b8-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




