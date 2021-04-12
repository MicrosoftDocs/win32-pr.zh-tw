---
title: '內建提供者內容識別碼 (Fwpmu .h) '
description: 內建提供者內容會識別要搭配安全通訊端使用的預設原則。
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464233"
---
# <a name="built-in-provider-context-identifiers"></a><span data-ttu-id="a82d3-103">內建提供者內容識別碼</span><span class="sxs-lookup"><span data-stu-id="a82d3-103">Built-in Provider Context Identifiers</span></span>

<span data-ttu-id="a82d3-104">內建于 Windows 篩選平台 (WFP) 的提供者內容識別碼，都是由 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="a82d3-104">The identifiers for the provider contexts that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="a82d3-105">這些內建提供者內容會識別要搭配安全通訊端使用的預設原則。</span><span class="sxs-lookup"><span data-stu-id="a82d3-105">These built-in provider contexts identify the default policies to use with secure sockets.</span></span>

<span data-ttu-id="a82d3-106">這些識別碼的定義如下。</span><span class="sxs-lookup"><span data-stu-id="a82d3-106">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="a82d3-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM \_ 提供者 \_ 內容 \_ 安全 \_ 通訊端 \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="a82d3-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a82d3-108">驗證的網際網路通訊協定 (AuthIP) 安全通訊端的主要模式預設原則。</span><span class="sxs-lookup"><span data-stu-id="a82d3-108">Authenticated Internet Protocol (AuthIP) main mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a82d3-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM \_ 提供者 \_ 內容 \_ 安全 \_ 通訊端 \_ IPSEC**</span><span class="sxs-lookup"><span data-stu-id="a82d3-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a82d3-110">網際網路通訊協定安全性 (IPsec) 安全通訊端的快速模式預設原則。</span><span class="sxs-lookup"><span data-stu-id="a82d3-110">Internet Protocol Security (IPsec) quick mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a82d3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a82d3-111">Requirements</span></span>



| <span data-ttu-id="a82d3-112">需求</span><span class="sxs-lookup"><span data-stu-id="a82d3-112">Requirement</span></span> | <span data-ttu-id="a82d3-113">值</span><span class="sxs-lookup"><span data-stu-id="a82d3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a82d3-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a82d3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a82d3-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a82d3-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a82d3-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a82d3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a82d3-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a82d3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a82d3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a82d3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a82d3-119"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="a82d3-119"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





