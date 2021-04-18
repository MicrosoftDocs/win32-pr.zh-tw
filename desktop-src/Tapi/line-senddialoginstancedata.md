---
description: TSPI LINE \_ SENDDIALOGINSTANCEDATA 訊息會使 TAPI \_ 在與 htDlgInst 相關聯的 UI DLL 中呼叫 TUISPI providerGenericDialogData 函式，並將 lpParams 所指向的參數區塊傳遞給長度為 dwSize 的。
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: 'LINE_SENDDIALOGINSTANCEDATA 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976247"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="7e69e-103">行 \_ SENDDIALOGINSTANCEDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="7e69e-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="7e69e-104">TSPI **LINE \_ SENDDIALOGINSTANCEDATA** 訊息會使 TAPI 在與 *HTDLGINST* 相關聯的 UI DLL 中呼叫 [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)函式，並 *將 lpParams 所* 指向的參數區塊傳遞給長度為 *dwSize* 的。</span><span class="sxs-lookup"><span data-stu-id="7e69e-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7e69e-105">參數</span><span class="sxs-lookup"><span data-stu-id="7e69e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e69e-106">*htDlgInst*</span><span class="sxs-lookup"><span data-stu-id="7e69e-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="7e69e-107">使用 [**行 \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)建立對話方塊實例時，傳回給服務提供者的 HTAPIDIALOGINSTANCE。</span><span class="sxs-lookup"><span data-stu-id="7e69e-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e69e-108">*lpParams*</span><span class="sxs-lookup"><span data-stu-id="7e69e-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="7e69e-109">傳遞給 UI DLL [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) 函式之提供者特定參數區塊的指標，其大小是由 *dwSize* 所指定。</span><span class="sxs-lookup"><span data-stu-id="7e69e-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="7e69e-110">如果這個參數設定為 **Null**，這就是立即關閉對話方塊的要求，清除 (UI DLL 不應該在此清除) 期間叫用 [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) 。</span><span class="sxs-lookup"><span data-stu-id="7e69e-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="7e69e-111">*dwSize*</span><span class="sxs-lookup"><span data-stu-id="7e69e-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7e69e-112">要傳達給 UI DLL 之參數區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e69e-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e69e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e69e-113">Requirements</span></span>



| <span data-ttu-id="7e69e-114">需求</span><span class="sxs-lookup"><span data-stu-id="7e69e-114">Requirement</span></span> | <span data-ttu-id="7e69e-115">值</span><span class="sxs-lookup"><span data-stu-id="7e69e-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7e69e-116">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7e69e-116">TAPI version</span></span><br/> | <span data-ttu-id="7e69e-117">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7e69e-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7e69e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7e69e-118">Header</span></span><br/>       | <dl> <span data-ttu-id="7e69e-119"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e69e-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e69e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e69e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e69e-121">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="7e69e-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="7e69e-122">**TUISPI \_ providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="7e69e-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="7e69e-123">**行 \_ CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="7e69e-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

