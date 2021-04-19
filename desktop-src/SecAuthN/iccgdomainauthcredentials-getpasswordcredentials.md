---
description: 傳回認證，以使用 Active Directory 驗證未加入網域的容器。
title: 'ICcgDomainAuthCredentials：： GetPasswordCredentials 方法 (ccgplugins .h) '
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990640"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="21fb6-103">ICcgDomainAuthCredentials：： GetPasswordCredentials 方法</span><span class="sxs-lookup"><span data-stu-id="21fb6-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="21fb6-104">傳回認證，以使用 Active Directory 驗證未加入網域的容器。</span><span class="sxs-lookup"><span data-stu-id="21fb6-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fb6-105">語法</span><span class="sxs-lookup"><span data-stu-id="21fb6-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="21fb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="21fb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21fb6-107">*pluginInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21fb6-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21fb6-108">容器執行時間傳入的輸入字串。</span><span class="sxs-lookup"><span data-stu-id="21fb6-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="21fb6-109">用戶端執行會使用提供的輸入字串來取出驗證認證，通常是從輸出參數中傳回的安全儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="21fb6-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="21fb6-110">輸入字串會提供給主機計算服務在認證規格檔案中 (HCS) 。</span><span class="sxs-lookup"><span data-stu-id="21fb6-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="21fb6-111">如需詳細資訊，請參閱「 **備註** 」一節。</span><span class="sxs-lookup"><span data-stu-id="21fb6-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="21fb6-112">*domainName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21fb6-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21fb6-113">認證的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb6-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="21fb6-114">使用者 *名稱* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21fb6-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21fb6-115">認證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="21fb6-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="21fb6-116">*密碼* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21fb6-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21fb6-117">認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="21fb6-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21fb6-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="21fb6-118">Return value</span></span>

<span data-ttu-id="21fb6-119">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="21fb6-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="21fb6-120">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="21fb6-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="21fb6-121">備註</span><span class="sxs-lookup"><span data-stu-id="21fb6-121">Remarks</span></span>

<span data-ttu-id="21fb6-122">您可以同時呼叫 API。</span><span class="sxs-lookup"><span data-stu-id="21fb6-122">The API may be called concurrently.</span></span> <span data-ttu-id="21fb6-123">因此，開發人員必須確保其實作為安全線程。</span><span class="sxs-lookup"><span data-stu-id="21fb6-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="21fb6-124">此外，COM 物件將會在進程外啟用，而且必須適當地註冊。</span><span class="sxs-lookup"><span data-stu-id="21fb6-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="21fb6-125">實作者必須針對其 COM CLSID 在 "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" 下新增金鑰。</span><span class="sxs-lookup"><span data-stu-id="21fb6-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="21fb6-126">對 "CCG\COMClasses" 的寫入存取權僅限於系統和系統管理員帳戶。</span><span class="sxs-lookup"><span data-stu-id="21fb6-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="21fb6-127">以下是範例認證規格檔案。</span><span class="sxs-lookup"><span data-stu-id="21fb6-127">The following is an example credential specification file.</span></span> <span data-ttu-id="21fb6-128">如需將此檔案提供給 Docker 的詳細資訊，請參閱 [使用 GMSA 執行容器](/virtualization/windowscontainers/manage-containers/gmsa-run-container)。</span><span class="sxs-lookup"><span data-stu-id="21fb6-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="21fb6-129">範例</span><span class="sxs-lookup"><span data-stu-id="21fb6-129">Examples</span></span>

<span data-ttu-id="21fb6-130">下列範例顯示簡單的 **ICcgDomainAuthCredentials** 執行。</span><span class="sxs-lookup"><span data-stu-id="21fb6-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="21fb6-131">請注意，為了方便說明，此範例只會剖析輸入字串來取得認證。</span><span class="sxs-lookup"><span data-stu-id="21fb6-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="21fb6-132">實際的執行會將認證儲存在安全的資料存放區中，並使用輸入字串來找出認證資訊。</span><span class="sxs-lookup"><span data-stu-id="21fb6-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="21fb6-133">此外，為了簡潔起見，已從這個範例中省略標準 COM 方法實作為。</span><span class="sxs-lookup"><span data-stu-id="21fb6-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="21fb6-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="21fb6-134">Requirements</span></span>




| <span data-ttu-id="21fb6-135">需求</span><span class="sxs-lookup"><span data-stu-id="21fb6-135">Requirement</span></span> | <span data-ttu-id="21fb6-136">值</span><span class="sxs-lookup"><span data-stu-id="21fb6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21fb6-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21fb6-137">Minimum supported server</span></span> | <span data-ttu-id="21fb6-138">Windows Server 版本 2004</span><span class="sxs-lookup"><span data-stu-id="21fb6-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="21fb6-139">標頭</span><span class="sxs-lookup"><span data-stu-id="21fb6-139">Header</span></span>                   | <span data-ttu-id="21fb6-140">ccgplugins。h</span><span class="sxs-lookup"><span data-stu-id="21fb6-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="21fb6-141">IID</span><span class="sxs-lookup"><span data-stu-id="21fb6-141">IID</span></span>                    | <span data-ttu-id="21fb6-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="21fb6-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

