---
title: 離線網域加入 IDL 定義
description: 離線網域加入 IDL 定義
ms.assetid: d495e2f0-5174-4d05-9297-4b4b0f200f08
ms.topic: article
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dec651c721cbe6bbf74123692137a01e528a82e5
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383166"
---
# <a name="offline-domain-join-idl-definitions"></a><span data-ttu-id="3ef79-103">離線網域加入 IDL 定義</span><span class="sxs-lookup"><span data-stu-id="3ef79-103">Offline Domain Join IDL Definitions</span></span>

## <a name="description"></a><span data-ttu-id="3ef79-104">Description</span><span class="sxs-lookup"><span data-stu-id="3ef79-104">Description</span></span>

<span data-ttu-id="3ef79-105">離線網域加入 (ODJ) 資料結構未在 C\C + + 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="3ef79-105">Offline Domain Join (ODJ) data structures are not defined in a C\C++ header file.</span></span>  <span data-ttu-id="3ef79-106">相反地，結構是以介面定義語言定義 (IDL) 格式，在編譯用於序列化和還原序列化之後。</span><span class="sxs-lookup"><span data-stu-id="3ef79-106">Instead, the structures are defined in Interface Definition Language (IDL) format which after compilation are used for serialization and deserialization.</span></span> <span data-ttu-id="3ef79-107">在 Windows 平臺上，這些結構的序列化和還原序列化會由下列 Win32 Api 自動處理：</span><span class="sxs-lookup"><span data-stu-id="3ef79-107">On the Windows platform serialization and deserialization of these structures is handled automatically by the following Win32 APIs:</span></span>

<span data-ttu-id="3ef79-108"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-108"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span></span>

<span data-ttu-id="3ef79-109"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-109"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a></span></span>

<span data-ttu-id="3ef79-110"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-110"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a></span></span>

<span data-ttu-id="3ef79-111"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-111"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a></span></span>

<span data-ttu-id="3ef79-112">在某些情況下（例如，與非 Windows 平臺進行 interop），可能需要手動序列化和還原序列化。</span><span class="sxs-lookup"><span data-stu-id="3ef79-112">In some situations, for example interop with non-Windows platforms, it may be necessary to do manual serialization and deserialization.</span></span> <span data-ttu-id="3ef79-113">本主題包含單一 IDL 編譯單位中所有 ODJ 資料結構的定義，並包含在 convienence 中。</span><span class="sxs-lookup"><span data-stu-id="3ef79-113">This topic contains definitions for all of the ODJ data structures in a single IDL compilation unit and is included for convienence.</span></span> <span data-ttu-id="3ef79-114">也會定義相符的應用程式佈建檔 (ACF) 定義。</span><span class="sxs-lookup"><span data-stu-id="3ef79-114">A matching Application Configuration File (ACF) definition is also defined.</span></span> <span data-ttu-id="3ef79-115">此內容未提供任何 SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ef79-115">This content is not provided as part of any SDK.</span></span> <span data-ttu-id="3ef79-116">因此，您應該將下列內容複寫到您的程式碼，並使用 IDL 編譯器進行編譯。</span><span class="sxs-lookup"><span data-stu-id="3ef79-116">Therefore the content below should be copied into your code and compiled with an IDL compiler.</span></span> <span data-ttu-id="3ef79-117">IDL 編譯器將會產生必要的 serialization\deserialization 存根函式，然後連結至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3ef79-117">The IDL compiler will produce the necessary serialization\deserialization stub functions, which are then linked into your application.</span></span> <span data-ttu-id="3ef79-118">如需類型序列化和還原序列化的詳細資訊，請參閱 <a href="/windows/win32/rpc/type-serialization">類型序列化</a> 。</span><span class="sxs-lookup"><span data-stu-id="3ef79-118">See <a href="/windows/win32/rpc/type-serialization">Type Serialization</a> for more details on how type serialization and deserialization.</span></span>

<span data-ttu-id="3ef79-119">如需詳細的成員檔，請參閱個別的結構區段。</span><span class="sxs-lookup"><span data-stu-id="3ef79-119">Refer to the individual structure sections for detailed member documentation.</span></span>

<span data-ttu-id="3ef79-120">如果您使用的是 Microsoft MIDL 編譯器，則應該指定下列旗標以最大化相容性：</span><span class="sxs-lookup"><span data-stu-id="3ef79-120">If you are using the Microsoft MIDL compiler, you should specify the following flags to maximize compatibility:</span></span>

<span data-ttu-id="3ef79-121">/char unsigned</span><span class="sxs-lookup"><span data-stu-id="3ef79-121">/char unsigned</span></span>

<span data-ttu-id="3ef79-122">/ms_ext</span><span class="sxs-lookup"><span data-stu-id="3ef79-122">/ms_ext</span></span>

<span data-ttu-id="3ef79-123">/c_ext</span><span class="sxs-lookup"><span data-stu-id="3ef79-123">/c_ext</span></span>

## <a name="odj-idl-file"></a><span data-ttu-id="3ef79-124">ODJ IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="3ef79-124">ODJ IDL File</span></span>

```C++
include "dsgetdc.h";

interface ODJ
{
    typedef struct _ODJ_BLOB
    {
        ULONG ulODJFormat;
        ULONG cbBlob;
        [size_is(cbBlob)] PBYTE pBlob;
    } ODJ_BLOB, *PODJ_BLOB;

    typedef struct _ODJ_PROVISION_DATA
    {
        ULONG ulVersion;
        ULONG ulcBlobs;
        [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
    } ODJ_PROVISION_DATA;

    typedef ODJ_PROVISION_DATA *PODJ_PROVISION_DATA;

    typedef struct _OP_BLOB
    {
        ULONG                       cbBlob;
        [size_is(cbBlob)]   PBYTE   pBlob;

    } OP_BLOB, *POP_BLOB;

    typedef struct _OP_PACKAGE_PART
    {
        GUID    PartType;
        ULONG   ulFlags;
        OP_BLOB Part;
        OP_BLOB Extension;
    } OP_PACKAGE_PART, *POP_PACKAGE_PART;

    typedef struct _OP_PACKAGE_PART_COLLECTION
    {
        ULONG                                 cParts;
        [size_is(cParts)]   POP_PACKAGE_PART  pParts;
        OP_BLOB                               Extension;
    } OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;

    typedef struct _OP_PACKAGE
    {
        GUID    EncryptionType;
        OP_BLOB EncryptionContext;
        OP_BLOB WrappedPartCollection;
        ULONG   cbDecryptedPartCollection;
        OP_BLOB Extension;
    } OP_PACKAGE, *POP_PACKAGE;

    typedef struct _SID_IDENTIFIER_AUTHORITY
    {
        UCHAR Value[6];
    } SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;

    typedef struct _ODJ_SID
    {
        UCHAR Revision;
        UCHAR SubAuthorityCount;
        SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
        [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
    }   ODJ_SID, *PODJ_SID;

    typedef struct _ODJ_UNICODE_STRING
    {
        USHORT Length;
        USHORT MaximumLength;
        [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
    } ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;

    typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
    {
        ODJ_UNICODE_STRING Name;
        ODJ_UNICODE_STRING DnsDomainName;
        ODJ_UNICODE_STRING DnsForestName;
        GUID DomainGuid;
        PODJ_SID Sid;
    }   ODJ_POLICY_DNS_DOMAIN_INFO;

    typedef struct _ODJ_WIN7BLOB
    {
        [string] wchar_t *lpDomain;
        [string] wchar_t *lpMachineName;
        [string] wchar_t *lpMachinePassword;
        ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
        DOMAIN_CONTROLLER_INFOW DcInfo;
        DWORD Options;
    } ODJ_WIN7BLOB;

    typedef ODJ_WIN7BLOB *PODJ_WIN7BLOB;

    cpp_quote("#define OP_JP2_FLAG_PERSISTENTSITE    0x00000001")

    typedef struct _OP_JOINPROV2_PART
    {
        DWORD     dwFlags;
        [string] wchar_t *lpNetbiosName;
        [string] wchar_t *lpSiteName;
        [string] wchar_t *lpPrimaryDNSDomain;

        DWORD             dwReserved;
        [string] wchar_t *lpReserved;
    } OP_JOINPROV2_PART, *POP_JOINPROV2_PART;

    typedef struct _OP_JOINPROV3_PART
    {
        DWORD Rid;
        [string] wchar_t *lpSid;
    } OP_JOINPROV3_PART, *POP_JOINPROV3_PART;

    typedef struct _OP_POLICY_ELEMENT
    {
        [string] wchar_t                *pKeyPath;
        [string] wchar_t                *pValueName;
        ULONG                           ulValueType;
        ULONG                           cbValueData;
        [size_is(cbValueData)]  PBYTE   pValueData;
    } OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;

    typedef struct _OP_POLICY_ELEMENT_LIST
    {
        [string] wchar_t                            *pSource;
        ULONG                                       ulRootKeyId;
        ULONG                                       cElements;
        [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
    } OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;

    typedef struct _OP_POLICY_PART
    {
        ULONG                                       cElementLists;
        [size_is(cElementLists)]
                            POP_POLICY_ELEMENT_LIST pElementLists;
        OP_BLOB                                     Extension;
    } OP_POLICY_PART, *POP_POLICY_PART;

    typedef struct _OP_CERT_PFX_STORE
    {
        [string] wchar_t            *pTemplateName;
        ULONG                       ulPrivateKeyExportPolicy;
        [string] wchar_t            *pPolicyServerUrl;
        ULONG                       ulPolicyServerUrlFlags;
        [string] wchar_t            *pPolicyServerId;
        ULONG                       cbPfx;
        [size_is(cbPfx)]    PBYTE   pPfx;
    } OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;

    typedef struct _OP_CERT_SST_STORE
    {
        ULONG                       StoreLocation;
        [string] wchar_t            *pStoreName;
        ULONG                       cbSst;
        [size_is(cbSst)]    PBYTE   pSst;
    } OP_CERT_SST_STORE, *POP_CERT_SST_STORE;

    typedef struct _OP_CERT_PART
    {
        ULONG                                       cPfxStores;
        [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
        ULONG                                       cSstStores;
        [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
        OP_BLOB                                     Extension;
    } OP_CERT_PART, *POP_CERT_PART;
}
```

## <a name="odj-acf-file"></a><span data-ttu-id="3ef79-125">ODJ ACF 檔</span><span class="sxs-lookup"><span data-stu-id="3ef79-125">ODJ ACF File</span></span>

```C++
[
    // If necessary for your application, see MIDL documentation for alternatives to explicit_handle
    explicit_handle
]
interface ODJ
{
    typedef [encode, decode] PODJ_WIN7BLOB;
    typedef [encode, decode] POP_JOINPROV2_PART;
    typedef [encode, decode] POP_JOINPROV3_PART;
    typedef [encode, decode] PODJ_PROVISION_DATA;
    typedef [encode, decode] POP_PACKAGE_PART;
    typedef [encode, decode] POP_PACKAGE_PART_COLLECTION;
    typedef [encode, decode] POP_PACKAGE;
    typedef [encode, decode] POP_POLICY_PART;
    typedef [encode, decode] POP_CERT_PART;
}
```

## <a name="see-also"></a><span data-ttu-id="3ef79-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ef79-126">See also</span></span>

<span data-ttu-id="3ef79-127"><a href="/windows/win32/midl/midl-start-page">Microsoft 介面定義語言</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-127"><a href="/windows/win32/midl/midl-start-page">Microsoft Interface Definition Language</a></span></span>

<span data-ttu-id="3ef79-128"><a href="/windows/win32/midl/midl-command-line-reference">MIDL Command-Line 參考</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-128"><a href="/windows/win32/midl/midl-command-line-reference">MIDL Command-Line Reference</a></span></span>

<span data-ttu-id="3ef79-129"><a href="/windows/win32/rpc/serialization-services">序列化服務</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-129"><a href="/windows/win32/rpc/serialization-services">Serialization Services</a></span></span>

<span data-ttu-id="3ef79-130"><a href="/windows/win32/rpc/type-serialization">類型序列化</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-130"><a href="/windows/win32/rpc/type-serialization">Type Serialization</a></span></span>

<span data-ttu-id="3ef79-131"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-131"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a></span></span>

<span data-ttu-id="3ef79-132"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-132"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a></span></span>

<span data-ttu-id="3ef79-133"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-133"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a></span></span>

<span data-ttu-id="3ef79-134"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a></span><span class="sxs-lookup"><span data-stu-id="3ef79-134"><a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a></span></span>
