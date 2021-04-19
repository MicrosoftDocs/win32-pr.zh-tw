---
description: TSPI LINE \_ CREATEDIALOGINSTANCE 訊息會使 TAPI 在服務提供者與在 \_ 應用程式內容中執行的 TUISPI providerGenericDialog 函式實例之間建立關聯。
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: 'LINE_CREATEDIALOGINSTANCE 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994084"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="ffc83-103">行 \_ CREATEDIALOGINSTANCE 訊息</span><span class="sxs-lookup"><span data-stu-id="ffc83-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="ffc83-104">TSPI **LINE \_ CREATEDIALOGINSTANCE** 訊息會使 TAPI 在服務提供者和 [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)函式的實例之間建立關聯，而該應用程式是在叫用非同步 TSPI 函式的應用程式內容中執行，而該應用程式是由 [**dwRequestID 所指向 TUISPICREATEDIALOGINSTANCEPARAMS 結構的**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) *lpTUISPICreateDialogInstanceParams* 參數所 *識別。*</span><span class="sxs-lookup"><span data-stu-id="ffc83-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ffc83-105">參數</span><span class="sxs-lookup"><span data-stu-id="ffc83-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc83-106">*hProvider*</span><span class="sxs-lookup"><span data-stu-id="ffc83-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="ffc83-107">提供給服務提供者的 ProviderHandle，做為 [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)的參數。</span><span class="sxs-lookup"><span data-stu-id="ffc83-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="ffc83-108">*lpTUISPICreateDialogInstanceParams*</span><span class="sxs-lookup"><span data-stu-id="ffc83-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="ffc83-109">[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ffc83-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffc83-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffc83-110">Requirements</span></span>



| <span data-ttu-id="ffc83-111">需求</span><span class="sxs-lookup"><span data-stu-id="ffc83-111">Requirement</span></span> | <span data-ttu-id="ffc83-112">值</span><span class="sxs-lookup"><span data-stu-id="ffc83-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ffc83-113">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ffc83-113">TAPI version</span></span><br/> | <span data-ttu-id="ffc83-114">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ffc83-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ffc83-115">標頭</span><span class="sxs-lookup"><span data-stu-id="ffc83-115">Header</span></span><br/>       | <dl> <span data-ttu-id="ffc83-116"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffc83-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc83-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffc83-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc83-118">**TSPI \_ providerEnumDevices**</span><span class="sxs-lookup"><span data-stu-id="ffc83-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="ffc83-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="ffc83-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

