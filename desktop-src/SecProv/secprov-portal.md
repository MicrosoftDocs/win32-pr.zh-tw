---
description: 安全性 WMI 提供者可用於 wmi 腳本，以及建立受管理的安全性提供者。
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: 安全性 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581986"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="8b1d3-103">安全性 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="8b1d3-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="8b1d3-104">目的</span><span class="sxs-lookup"><span data-stu-id="8b1d3-104">Purpose</span></span>

<span data-ttu-id="8b1d3-105">安全性 wmi 提供者可讓系統管理員和程式設計人員使用) Windows Management Instrumentation WMI (，設定 BitLocker 磁碟機加密 (的) 和可信賴平臺模組 (TPM) 。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8b1d3-106">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="8b1d3-106">Developer audience</span></span>

<span data-ttu-id="8b1d3-107">本檔指定的 WMI 提供者介面可用於管理和設定 BitLocker 磁碟機加密 (的) 以及) server 2008 R2 上的信賴平臺模組 (TPM Windows 以及適用于伺服器的 Windows server 2008，以及 Windows 7 和 Windows Vista （適用于用戶端電腦）。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="8b1d3-108">它的目的是要讓撰寫腳本、使用者介面專案或其他的系統管理工具或 TPM 進行讀取。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8b1d3-109">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="8b1d3-109">Run-time requirements</span></span>

<span data-ttu-id="8b1d3-110">安全性 WMI 提供者需要使用每個提供者和支援的作業系統指定的 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="8b1d3-111">最低作業系統是 Windows Server 2008 或 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8b1d3-112">BitLocker 磁碟機加密僅適用于 Windows vista Enterprise 和 Windows vista 旗艦版 Windows vista。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="8b1d3-113">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8b1d3-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="8b1d3-114">In this section</span></span>



| <span data-ttu-id="8b1d3-115">主題</span><span class="sxs-lookup"><span data-stu-id="8b1d3-115">Topic</span></span>                                                                               | <span data-ttu-id="8b1d3-116">描述</span><span class="sxs-lookup"><span data-stu-id="8b1d3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="8b1d3-117">關於安全性 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="8b1d3-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="8b1d3-118">安全性 WMI 提供者的簡短總覽。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="8b1d3-119">安全性 WMI 提供者參考</span><span class="sxs-lookup"><span data-stu-id="8b1d3-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="8b1d3-120">安全性 WMI 提供者的參考檔。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="8b1d3-121">其他資源</span><span class="sxs-lookup"><span data-stu-id="8b1d3-121">Additional resources</span></span>

<span data-ttu-id="8b1d3-122">以下是其他資源。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-122">The following are additional resources.</span></span>



| <span data-ttu-id="8b1d3-123">資源</span><span class="sxs-lookup"><span data-stu-id="8b1d3-123">Resource</span></span>     | <span data-ttu-id="8b1d3-124">描述</span><span class="sxs-lookup"><span data-stu-id="8b1d3-124">Description</span></span>                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1d3-125">類別</span><span class="sxs-lookup"><span data-stu-id="8b1d3-125">Classes</span></span>      | <span data-ttu-id="8b1d3-126">如需有關安全性 WMI 提供者的詳細資訊，請參閱 [**win32 \_ EncryptableVolume**](win32-encryptablevolume.md) 和 [**win32 \_ Tpm**](win32-tpm.md)。</span><span class="sxs-lookup"><span data-stu-id="8b1d3-126">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span> |



 

 

 




