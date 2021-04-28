---
description: Commit 方法的 IWICFastMetadataEncoder_Commit_Proxy 函數 Proxy 函式。
ms.assetid: 5b3b90ad-9d67-4fbd-b01e-c7478df8dd45
title: IWICFastMetadataEncoder_Commit_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 848ed74ec9c9bb490065935bd94cae7a35d02db2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097186"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a><span data-ttu-id="fbea2-103">IWICFastMetadataEncoder \_ Commit \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="fbea2-103">IWICFastMetadataEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="fbea2-104">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit)方法的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="fbea2-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbea2-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbea2-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="fbea2-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbea2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbea2-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="fbea2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbea2-108">類型： **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span><span class="sxs-lookup"><span data-stu-id="fbea2-108">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span></span>

<span data-ttu-id="fbea2-109">這個 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="fbea2-109">Pointer to this [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbea2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbea2-110">Return value</span></span>

<span data-ttu-id="fbea2-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fbea2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="fbea2-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fbea2-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbea2-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fbea2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbea2-114">備註</span><span class="sxs-lookup"><span data-stu-id="fbea2-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fbea2-115">需求</span><span class="sxs-lookup"><span data-stu-id="fbea2-115">Requirements</span></span>



| <span data-ttu-id="fbea2-116">需求</span><span class="sxs-lookup"><span data-stu-id="fbea2-116">Requirement</span></span> | <span data-ttu-id="fbea2-117">值</span><span class="sxs-lookup"><span data-stu-id="fbea2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbea2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbea2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbea2-119">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbea2-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fbea2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbea2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbea2-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbea2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fbea2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fbea2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbea2-123"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbea2-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




