---
description: 實行 IAxiService 和 IeAxiServiceCallback 介面。
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: CIeAxiInstallerService 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943503"
---
# <a name="cieaxiinstallerservice-object"></a><span data-ttu-id="243cd-103">CIeAxiInstallerService 物件</span><span class="sxs-lookup"><span data-stu-id="243cd-103">CIeAxiInstallerService object</span></span>

<span data-ttu-id="243cd-104">**CIeAxiInstallerService** 物件會實 [**IAxiService**](ieaxiservice.md)和 [**IeAxiServiceCallback**](ieaxiservicecallback.md)介面。</span><span class="sxs-lookup"><span data-stu-id="243cd-104">The **CIeAxiInstallerService** object implements the [**IAxiService**](ieaxiservice.md) and [**IeAxiServiceCallback**](ieaxiservicecallback.md) interfaces.</span></span>

<span data-ttu-id="243cd-105">此物件未在公用標頭中宣告。</span><span class="sxs-lookup"><span data-stu-id="243cd-105">This object is not declared in a public header.</span></span> <span data-ttu-id="243cd-106">應用程式必須自行定義。</span><span class="sxs-lookup"><span data-stu-id="243cd-106">Applications must define it themselves.</span></span> <span data-ttu-id="243cd-107">下列介面定義語言 (IDL) 片段描述這個物件，包括其 CLSID。</span><span class="sxs-lookup"><span data-stu-id="243cd-107">The following Interface Definition Language (IDL) fragment describes this object, including its CLSID.</span></span>

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a><span data-ttu-id="243cd-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="243cd-108">Requirements</span></span>



| <span data-ttu-id="243cd-109">需求</span><span class="sxs-lookup"><span data-stu-id="243cd-109">Requirement</span></span> | <span data-ttu-id="243cd-110">值</span><span class="sxs-lookup"><span data-stu-id="243cd-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="243cd-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="243cd-111">Minimum supported client</span></span><br/> | <span data-ttu-id="243cd-112">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="243cd-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="243cd-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="243cd-113">Minimum supported server</span></span><br/> | <span data-ttu-id="243cd-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="243cd-114">None supported</span></span><br/>                                                                                 |



## <a name="see-also"></a><span data-ttu-id="243cd-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="243cd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243cd-116">**IAxiService**</span><span class="sxs-lookup"><span data-stu-id="243cd-116">**IAxiService**</span></span>](ieaxiservice.md)
</dt> <dt>

[<span data-ttu-id="243cd-117">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="243cd-117">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

 




