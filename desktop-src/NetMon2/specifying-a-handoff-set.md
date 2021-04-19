---
description: 遞交集會指定遵循通訊協定的通訊協定。 只有當剖析器可以從通訊協定實例中的資料識別下一個通訊協定時，剖析器才會使用一組遞交集。
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: 指定遞交集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970227"
---
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="abb93-104">指定遞交集</span><span class="sxs-lookup"><span data-stu-id="abb93-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="abb93-105">遞交集會指定遵循通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="abb93-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="abb93-106">只有當剖析器可以從通訊協定實例中的資料識別下一個通訊協定時，剖析器才會使用一組遞交集。</span><span class="sxs-lookup"><span data-stu-id="abb93-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="abb93-107">例如，TCP 通訊協定具有埠屬性，可識別 TCP 通訊協定後面的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="abb93-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="abb93-108">屬性值為20表示下一個通訊協定是 FTP。</span><span class="sxs-lookup"><span data-stu-id="abb93-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="abb93-109">屬性值53表示下一個通訊協定是 DNS。</span><span class="sxs-lookup"><span data-stu-id="abb93-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="abb93-110">因為 port 屬性會識別接下來的通訊協定，所以 TCP 剖析器可以使用下列的遞交集來取得埠屬性指定之通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="abb93-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

<span data-ttu-id="abb93-111">遞交集會儲存在剖析器 INI 檔案中。</span><span class="sxs-lookup"><span data-stu-id="abb93-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="abb93-112">例如，先前的 TCP 遞交集位於 tcpip.ini 檔案中。</span><span class="sxs-lookup"><span data-stu-id="abb93-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="abb93-113">請注意，如果剖析器 DLL 支援多個通訊協定，則每個使用遞交集的剖析器在 INI 檔案中都有自己的位置。</span><span class="sxs-lookup"><span data-stu-id="abb93-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="abb93-114">在 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) 函數的執行期間，會指定遞交集資訊。</span><span class="sxs-lookup"><span data-stu-id="abb93-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="abb93-115">剖析器可以指定剖析器通訊協定之前的通訊協定，以及遵循剖析器通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="abb93-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="abb93-116">網路監視器會採用之前的所有通訊協定，並將剖析器通訊協定新增至剖析器 INI 檔案中的下列設定區段—適用于上述每個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="abb93-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="abb93-117">網路監視器會在剖析器 INI 檔案的 [遞交集] 區段中儲存遵循的通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="abb93-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="abb93-118">網路監視器會將遞交集資訊儲存在剖析器 INI 檔案中，但剖析器不會直接存取 INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="abb93-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="abb93-119">若要使用遞交集中的資訊，剖析器會呼叫 [**CreateHandoffTable**](createhandofftable.md) 函數來建立遞交資料表。</span><span class="sxs-lookup"><span data-stu-id="abb93-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="abb93-120">通常，當剖析器註冊通訊協定時，就會建立遞交資料表。</span><span class="sxs-lookup"><span data-stu-id="abb93-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="abb93-121">註冊通訊協定之後，網路監視器會建立剖析器可以使用的一個遞交集資料表。</span><span class="sxs-lookup"><span data-stu-id="abb93-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="abb93-122">剖析器會在辨識資料時使用其交付集。</span><span class="sxs-lookup"><span data-stu-id="abb93-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="abb93-123">首先，剖析器會讀取識別下一個通訊協定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="abb93-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="abb93-124">然後，剖析器會呼叫 [**GetProtocolFromTable**](getprotocolfromtable.md) 來取得下一個通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="abb93-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="abb93-125">最後，剖析器會將指標傳回至 [**RecognizeFrame**](recognizeframe.md)的 *phNextProtocol* 參數中的控制碼。</span><span class="sxs-lookup"><span data-stu-id="abb93-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 



