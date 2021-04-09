---
description: 由 IeAxiSystemInstaller 介面呼叫，以確認可以安裝 ActiveX 物件。
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: IeAxiServiceCallback 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852908"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="30d00-103">IeAxiServiceCallback 介面</span><span class="sxs-lookup"><span data-stu-id="30d00-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="30d00-104">**IeAxiServiceCallback** 介面會由 [**IeAxiSystemInstaller**](ieaxisysteminstaller.md)介面呼叫，以確認可以安裝 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="30d00-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="30d00-105">[**CIeAxiInstallerService**](cieaxiinstallerservice.md)類別會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="30d00-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="30d00-106">未在公用標頭中宣告此介面。</span><span class="sxs-lookup"><span data-stu-id="30d00-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="30d00-107">應用程式必須自行定義。</span><span class="sxs-lookup"><span data-stu-id="30d00-107">Applications must define it themselves.</span></span> <span data-ttu-id="30d00-108">下列介面定義語言 (IDL) 片段描述這個介面，包括其 IID。</span><span class="sxs-lookup"><span data-stu-id="30d00-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="30d00-109">成員</span><span class="sxs-lookup"><span data-stu-id="30d00-109">Members</span></span>

<span data-ttu-id="30d00-110">**IeAxiServiceCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="30d00-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="30d00-111">**IeAxiServiceCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="30d00-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="30d00-112">方法</span><span class="sxs-lookup"><span data-stu-id="30d00-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="30d00-113">方法</span><span class="sxs-lookup"><span data-stu-id="30d00-113">Methods</span></span>

<span data-ttu-id="30d00-114">**IeAxiServiceCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="30d00-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="30d00-115">方法</span><span class="sxs-lookup"><span data-stu-id="30d00-115">Method</span></span>                                                | <span data-ttu-id="30d00-116">描述</span><span class="sxs-lookup"><span data-stu-id="30d00-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30d00-117">**VerifyFile**</span><span class="sxs-lookup"><span data-stu-id="30d00-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="30d00-118">針對指定的 ActiveX 物件執行安全性檢查，並傳回下載對應 .cab 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="30d00-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30d00-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="30d00-119">Requirements</span></span>



| <span data-ttu-id="30d00-120">需求</span><span class="sxs-lookup"><span data-stu-id="30d00-120">Requirement</span></span> | <span data-ttu-id="30d00-121">值</span><span class="sxs-lookup"><span data-stu-id="30d00-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30d00-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30d00-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30d00-123">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30d00-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="30d00-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30d00-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30d00-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="30d00-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="30d00-126">IID</span><span class="sxs-lookup"><span data-stu-id="30d00-126">IID</span></span><br/>                      | <span data-ttu-id="30d00-127">IID \_ IeAxiServiceCallback 定義為1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="30d00-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

