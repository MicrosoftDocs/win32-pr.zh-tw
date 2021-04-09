---
title: 端點屬性
description: '\ Endpoint \ 屬性（attribute）會指定已知的埠或埠 (通訊端點，) 在哪些伺服器上接聽呼叫。'
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- endpoint 屬性 MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842135"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="f0c55-104">端點屬性</span><span class="sxs-lookup"><span data-stu-id="f0c55-104">endpoint attribute</span></span>

<span data-ttu-id="f0c55-105">**\[ 端點 \]** 屬性會指定已知的埠或埠 (通訊端點，) 在其上，介面的伺服器會接聽呼叫。</span><span class="sxs-lookup"><span data-stu-id="f0c55-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="f0c55-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0c55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c55-107">*通訊協定順序*</span><span class="sxs-lookup"><span data-stu-id="f0c55-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c55-108">指定代表 RPC 通訊協定 (的有效組合的字元字串，例如 "ncacn" ) 、傳輸通訊協定 (例如 "tcp" ) 和網路通訊協定 (例如 "ip" ) 。</span><span class="sxs-lookup"><span data-stu-id="f0c55-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="f0c55-109">如需有效通訊協定順序的清單，請參閱 [通訊協定順序常數](/windows/desktop/Rpc/protocol-sequence-constants)。</span><span class="sxs-lookup"><span data-stu-id="f0c55-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="f0c55-110">*端點-埠*</span><span class="sxs-lookup"><span data-stu-id="f0c55-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c55-111">指定表示指定之通訊協定系列之端點指定的字串。</span><span class="sxs-lookup"><span data-stu-id="f0c55-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="f0c55-112">埠字串的語法為每個通訊協定順序所特有。</span><span class="sxs-lookup"><span data-stu-id="f0c55-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0c55-113">備註</span><span class="sxs-lookup"><span data-stu-id="f0c55-113">Remarks</span></span>

<span data-ttu-id="f0c55-114">**\[ 端點 \]** 屬性會指定傳輸家族，例如 tcp/ip 連接導向的通訊協定、NetBIOS 連接導向的通訊協定，或具名管道連接導向的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f0c55-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="f0c55-115">**\[ 端點 \]** 屬性的使用與其他新增端點的方法一致，而且不提供端點的其他或特殊服務，只會提供呼叫 API 的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f0c55-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="f0c55-116">在中指定端點。IDL 介面定義不會將介面的存取限制為指定的端點。</span><span class="sxs-lookup"><span data-stu-id="f0c55-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="f0c55-117">將端點加入至。IDL 介面定義允許透過該進程中的任何端點來呼叫介面，並允許在該進程中使用端點來呼叫其他介面。</span><span class="sxs-lookup"><span data-stu-id="f0c55-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="f0c55-118">*通訊協定序列* 值會決定 *端點埠* 的有效值。</span><span class="sxs-lookup"><span data-stu-id="f0c55-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="f0c55-119">MIDL 編譯器只會檢查 *端點埠* 專案的一般語法。</span><span class="sxs-lookup"><span data-stu-id="f0c55-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="f0c55-120">執行時間程式庫會報告埠規格錯誤。</span><span class="sxs-lookup"><span data-stu-id="f0c55-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="f0c55-121">如需每個通訊協定順序之允許值的相關資訊，請參閱 [通訊協定順序常數](/windows/desktop/Rpc/protocol-sequence-constants)。</span><span class="sxs-lookup"><span data-stu-id="f0c55-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="f0c55-122">Microsoft RPC： **ncacn \_ osi \_ dna** 和 **ncadg \_ dds** 提供的 MIDL 編譯器不支援 DCE 指定的下列通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="f0c55-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="f0c55-123">請確定您已正確地在端點中括住反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="f0c55-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="f0c55-124">當端點是具名管道時，通常會發生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="f0c55-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="f0c55-125">IDL 檔案中指定的端點資訊是由 RPC 執行時間函式 [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) 和 [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)所使用。</span><span class="sxs-lookup"><span data-stu-id="f0c55-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="f0c55-126">範例</span><span class="sxs-lookup"><span data-stu-id="f0c55-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="f0c55-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0c55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c55-128"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="f0c55-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f0c55-129">**RpcServerUseAllProtseqsIf**</span><span class="sxs-lookup"><span data-stu-id="f0c55-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="f0c55-130">**RpcServerUseProtseqIf**</span><span class="sxs-lookup"><span data-stu-id="f0c55-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 