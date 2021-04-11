---
description: 呼叫資料是大小可變大小的緩衝區，可用於累積通訊會話的相關資訊。 此資訊可供擁有或監視會話的所有應用程式使用。
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: 呼叫資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318880"
---
# <a name="call-data"></a><span data-ttu-id="519d8-104">呼叫資料</span><span class="sxs-lookup"><span data-stu-id="519d8-104">Call Data</span></span>

<span data-ttu-id="519d8-105">呼叫資料是大小可變大小的緩衝區，可用於累積通訊會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="519d8-105">Call data is a variably sized buffer that can be used to accumulate information about a communications session.</span></span> <span data-ttu-id="519d8-106">此資訊可供擁有或監視會話的所有應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="519d8-106">This information becomes available to all applications that own or monitor the session.</span></span>

<span data-ttu-id="519d8-107">例如，傳入會話的初始處理常式可能會要求並將用戶端帳戶資訊輸入至呼叫資料緩衝區，然後後續處理常式不需要重複要求。</span><span class="sxs-lookup"><span data-stu-id="519d8-107">For example, the initial handler of an incoming session might request and enter client account information into a call data buffer, and then subsequent handlers would not have to repeat the request.</span></span>

<span data-ttu-id="519d8-108">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="519d8-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="519d8-109">**TAPI 2.x：** 請參閱 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** 和 **dwCallDataOffset** 成員， [**LINE \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* 設定為 LINECALLINFOSTATE \_ CALLDATA) 。</span><span class="sxs-lookup"><span data-stu-id="519d8-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_CALLDATA).</span></span>

<span data-ttu-id="519d8-110">**TAPI 3.x：** 請參閱 [**ITCallInfo：:P CALLINFO \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ CALLDATABUFFER** 成員的 [**\_ 緩衝區**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)) ;[**ITCallInfoChangeEvent：： get \_原因會**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause)傳回 [**CALLINFOCHANGE \_ 原因**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause)的 **CIC \_ CALLDATA** 成員。</span><span class="sxs-lookup"><span data-stu-id="519d8-110">**TAPI 3.x:** See [**ITCallInfo::put\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB\_CALLDATABUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) returns the **CIC\_CALLDATA** member of [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span></span>

 

 
