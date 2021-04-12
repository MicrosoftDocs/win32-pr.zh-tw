---
description: " (SNMP) 提供者的簡易網路管理通訊協定，可讓用戶端應用程式透過 Windows Management Instrumentation (WMI) 來存取 SNMP 資訊。"
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI 和 SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195233"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="10af1-103">WMI 和 SNMP</span><span class="sxs-lookup"><span data-stu-id="10af1-103">WMI and SNMP</span></span>

<span data-ttu-id="10af1-104"> (SNMP) 提供者的簡易網路管理通訊協定，可讓用戶端應用程式透過 Windows Management Instrumentation (WMI) 來存取 SNMP 資訊。</span><span class="sxs-lookup"><span data-stu-id="10af1-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="10af1-105">SNMP 提供者預設不會安裝。</span><span class="sxs-lookup"><span data-stu-id="10af1-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="10af1-106">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="10af1-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="10af1-107">簡易網路管理通訊協定 (SNMP) 使用架構來定義物件。</span><span class="sxs-lookup"><span data-stu-id="10af1-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="10af1-108">架構不同于 WMI 中使用的架構。</span><span class="sxs-lookup"><span data-stu-id="10af1-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="10af1-109">SNMPv1 和 SNMPv2C 架構稱為 (SMI-S) 管理資訊的結構，並封裝為管理資訊基礎 (MIB) 檔。</span><span class="sxs-lookup"><span data-stu-id="10af1-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="10af1-110">MIB 檔案會使用標準語言來定義物件-抽象語法標記法 1 (asn.1) ），以及一些巨集定義，做為描述物件的範本。</span><span class="sxs-lookup"><span data-stu-id="10af1-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="10af1-111">宏提供的資訊包括物件名稱、識別碼、語法、描述、存取權限、通訊協定作業和通訊協定編碼。</span><span class="sxs-lookup"><span data-stu-id="10af1-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="10af1-112">下表列出 SNMP 提供者如何處理 MIB 物件的不同層面。</span><span class="sxs-lookup"><span data-stu-id="10af1-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="10af1-113">主題</span><span class="sxs-lookup"><span data-stu-id="10af1-113">Topic</span></span>                                                    | <span data-ttu-id="10af1-114">描述</span><span class="sxs-lookup"><span data-stu-id="10af1-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="10af1-115">通知類型宏</span><span class="sxs-lookup"><span data-stu-id="10af1-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="10af1-116">**通知類型** 宏如何從 SNMP 對應至 WMI。</span><span class="sxs-lookup"><span data-stu-id="10af1-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="10af1-117">OBJECT 類型宏</span><span class="sxs-lookup"><span data-stu-id="10af1-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="10af1-118">**物件類型** 宏如何從 SNMP 對應至 WMI。</span><span class="sxs-lookup"><span data-stu-id="10af1-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="10af1-119">文字慣例宏</span><span class="sxs-lookup"><span data-stu-id="10af1-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="10af1-120">**文字慣例** 宏如何從 SNMP 對應至 WMI。</span><span class="sxs-lookup"><span data-stu-id="10af1-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="10af1-121">TRAP 類型宏</span><span class="sxs-lookup"><span data-stu-id="10af1-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="10af1-122">**陷阱類型** 宏如何從 SNMP 對應至 WMI。</span><span class="sxs-lookup"><span data-stu-id="10af1-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="10af1-123">SNMP 提供者隨附可將 MIB 物件轉譯成 WMI 物件的編譯器。</span><span class="sxs-lookup"><span data-stu-id="10af1-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="10af1-124">SNMP 編譯器也可以輸出錯誤或其他訊息。</span><span class="sxs-lookup"><span data-stu-id="10af1-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="10af1-125">如需詳細資訊，請參閱 [SNMP 編譯器錯誤訊息](snmp-compiler-error-messages.md) 和 [一般資訊訊息](general-information-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="10af1-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="10af1-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="10af1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10af1-127">WMI 參考</span><span class="sxs-lookup"><span data-stu-id="10af1-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="10af1-128">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="10af1-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



