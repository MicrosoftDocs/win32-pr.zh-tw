---
description: 您可以使用 identity Manager 和群組 Api 中的身分識別匯入和匯出函式，將對等身分識別和群組設定檔案匯入和匯出至另一個端點。
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: 身分識別和群組設定匯入和匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693043"
---
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="b2c6f-103">身分識別和群組設定匯入和匯出</span><span class="sxs-lookup"><span data-stu-id="b2c6f-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="b2c6f-104">您可以使用 identity Manager 和群組 Api 中的身分識別匯入和匯出函式，將對等身分識別和群組設定檔案匯入和匯出至另一個端點。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="b2c6f-105">這些功能很有用，因為它們可讓使用者快速且方便地將身分識別和群組設定資訊從一部電腦匯出到另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="b2c6f-106">匯入和匯出對等身分識別資料</span><span class="sxs-lookup"><span data-stu-id="b2c6f-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="b2c6f-107">藉由呼叫 [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) 以及要匯出的身分識別名稱，以及用來加密相關聯認證的密碼，匯出對等的身分識別資料。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="b2c6f-108">此函式會傳回 XML 字串，其中包含對等的身分識別名稱，以及該特定身分識別的加密認證，然後使用外部傳輸機制（例如電子郵件）將其傳遞至不同的電腦。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="b2c6f-109">下列範例會顯示 XML 字串的格式：</span><span class="sxs-lookup"><span data-stu-id="b2c6f-109">The following example shows you the format of the XML string:</span></span>

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

<span data-ttu-id="b2c6f-110">您可以藉由呼叫 [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)來抓取匯出的身分識別資料，並以前一次呼叫 [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)中提供的密碼傳入 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="b2c6f-111">此函式會傳回匯入之身分識別的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="b2c6f-112">匯入的身分識別名稱和認證可以像 [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) 或 [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)所傳回的身分識別名稱一樣使用。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="b2c6f-113">呼叫 [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)時，應用程式或 API 使用者必須提供具有足夠長度的強式密碼。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="b2c6f-114">這點很重要，因為匯入的身分識別資料包含身分識別的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="b2c6f-115">匯入和匯出群組身分識別設定</span><span class="sxs-lookup"><span data-stu-id="b2c6f-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="b2c6f-116">對等群組可讓對等使用特定的匯入和匯出 Api，將群組設定資料從某個端點匯出至另一個端點。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="b2c6f-117">若要匯入設定資料，執行匯入 (之對等的身分識別，以及先前執行匯出) 的電腦必須存在於要匯入設定資料的電腦上。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="b2c6f-118">您可以藉由使用本主題上一節中指定的方法來匯出和匯入此身分識別：匯 [入和匯出對等身分識別資料](#importing-and-exporting-peer-identity-data)。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="b2c6f-119">群組設定資料包含身分識別的所有資訊，以從新的端點加入群組。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="b2c6f-120">具體而言，設定資料包含 GMC 鏈、群組對等名稱、雲端名稱、範圍，以及一組 PNRP 特定旗標。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="b2c6f-121">若為擁有群組的身分識別，群組設定資訊中就會包含該群組的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="b2c6f-122">呼叫 [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)時，應用程式或 API 使用者必須提供具有足夠長度的強式密碼。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="b2c6f-123">這點很重要，因為匯入的身分識別資料包含群組的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="b2c6f-124">若要匯出目前的對等群組設定，請呼叫 [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)，將控制碼傳遞給群組 (由先前的 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)、 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)或 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) 呼叫取得，以及用來加密和保護設定檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="b2c6f-125">此函式會傳回 XML 字串，其中包含下列範例格式的設定，接著可以使用外部傳輸機制（例如電子郵件）將其寫入檔案並傳遞至另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

<span data-ttu-id="b2c6f-126">以 XML 字串形式取得群組設定之後，您可以藉由呼叫 [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) 與設定 XML 字串以及提供給 [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)的特定密碼，來匯入群組。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="b2c6f-127">此函式會傳回身分識別名稱和群組對等名稱，然後將其提供給 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) ，並連接到建立的群組。</span><span class="sxs-lookup"><span data-stu-id="b2c6f-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



