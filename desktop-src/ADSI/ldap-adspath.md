---
title: LDAP ADsPath
description: 本主題說明您應該針對 LDAP ADsPath 使用的語法。
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP ADsPath
- ADsPath、LDAP、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683109"
---
# <a name="ldap-adspath"></a><span data-ttu-id="de5e7-105">LDAP ADsPath</span><span class="sxs-lookup"><span data-stu-id="de5e7-105">LDAP ADsPath</span></span>

<span data-ttu-id="de5e7-106">Microsoft LDAP 提供者 ADsPath 需要下列格式。</span><span class="sxs-lookup"><span data-stu-id="de5e7-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="de5e7-107">左和右方括弧字元 (\[ \]) 表示選擇性參數，而不是系結字串的常值部分。</span><span class="sxs-lookup"><span data-stu-id="de5e7-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="de5e7-108">「主機名稱」可以是電腦名稱稱、IP 位址或功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="de5e7-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="de5e7-109">您也可以在系結字串中指定伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="de5e7-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="de5e7-110">大部分的 LDAP 提供者都遵循需要指定伺服器名稱的模型。</span><span class="sxs-lookup"><span data-stu-id="de5e7-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="de5e7-111">"PortNumber" 會指定要用於連接的埠。</span><span class="sxs-lookup"><span data-stu-id="de5e7-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="de5e7-112">如果未指定埠號碼，LDAP 提供者會使用預設的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="de5e7-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="de5e7-113">如果使用 ssl 連線，預設的埠號碼為389（如果未使用 SSL 連線）或636（如果使用 SSL 連線）。</span><span class="sxs-lookup"><span data-stu-id="de5e7-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="de5e7-114">"DistinguishedName" 指定特定物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="de5e7-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="de5e7-115">指定之物件的辨別名稱一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="de5e7-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="de5e7-116">下表列出系結字串的範例。</span><span class="sxs-lookup"><span data-stu-id="de5e7-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="de5e7-117">LDAP ADsPath 範例</span><span class="sxs-lookup"><span data-stu-id="de5e7-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="de5e7-118">Description</span><span class="sxs-lookup"><span data-stu-id="de5e7-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="de5e7-119">Ldap：</span><span class="sxs-lookup"><span data-stu-id="de5e7-119">LDAP:</span></span>                                                     | <span data-ttu-id="de5e7-120">系結至 LDAP 命名空間的根目錄。</span><span class="sxs-lookup"><span data-stu-id="de5e7-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="de5e7-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="de5e7-121">LDAP://server01</span></span>                                           | <span data-ttu-id="de5e7-122">系結至特定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="de5e7-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="de5e7-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="de5e7-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="de5e7-124">使用指定的埠號碼系結至特定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="de5e7-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="de5e7-125">LDAP：//CN = Jeff Smith，CN = users，DC = fabrikam，DC = com</span><span class="sxs-lookup"><span data-stu-id="de5e7-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="de5e7-126">系結至特定物件。</span><span class="sxs-lookup"><span data-stu-id="de5e7-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="de5e7-127">LDAP://server01/CN=Jeff Smith，CN = users，DC = fabrikam，DC = com</span><span class="sxs-lookup"><span data-stu-id="de5e7-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="de5e7-128">透過特定伺服器系結至特定物件。</span><span class="sxs-lookup"><span data-stu-id="de5e7-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="de5e7-129">如果成功完成特定目錄要求時需要 Kerberos 驗證，系結字串必須使用無伺服器 ADsPath，例如 LDAP：//CN = Jeff Smith，CN = users，DC = fabrikam，DC = com，或者必須使用具有完整 DNS 伺服器名稱的 ADsPath，例如 LDAP://server01.fabrikam.com/CN=Jeff Smith、CN = users，DC = fabrikam，DC = com。</span><span class="sxs-lookup"><span data-stu-id="de5e7-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="de5e7-130">使用一般 NETBIOS 名稱或簡短 DNS 名稱（例如，使用名稱 server01 而非 server01.fabrikam.com）系結至伺服器，並不保證會產生 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="de5e7-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="de5e7-131">如需 LDAP 系結字串的詳細資訊和範例，以及可在 LDAP 系結字串中使用之特殊字元的描述，請參閱 LDAP ADsPath。</span><span class="sxs-lookup"><span data-stu-id="de5e7-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="de5e7-132">**Windows 2000 SP1 和更新版本：** 使用 LDAP 提供者時，如果系結字串包含伺服器名稱，您可以使用 **ADS \_ 伺服器 \_** 系結旗標搭配 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函式或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法來提高效能。</span><span class="sxs-lookup"><span data-stu-id="de5e7-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="de5e7-133">**ADS \_ 伺服器 \_** 系結旗標表示指定了伺服器名稱，可讓 ADSI 避開其他不必要的網路流量。</span><span class="sxs-lookup"><span data-stu-id="de5e7-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="de5e7-134">LDAP 特殊字元</span><span class="sxs-lookup"><span data-stu-id="de5e7-134">LDAP Special Characters</span></span>

<span data-ttu-id="de5e7-135">LDAP 有數個特殊字元，這些特殊字元已保留供 LDAP API 使用。</span><span class="sxs-lookup"><span data-stu-id="de5e7-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="de5e7-136">您可以在 [辨別名稱](/previous-versions/windows/desktop/ldap/distinguished-names)中找到特殊字元清單。</span><span class="sxs-lookup"><span data-stu-id="de5e7-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="de5e7-137">若要在 ADsPath 中使用其中一個字元，而不產生錯誤，字元前面必須加上反斜線 (\\) 字元。</span><span class="sxs-lookup"><span data-stu-id="de5e7-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="de5e7-138">這就是所謂的 *轉義* 字元。</span><span class="sxs-lookup"><span data-stu-id="de5e7-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="de5e7-139">例如，如果以 "，" 形式提供使用者名稱 <last name> <first name> ，則必須將名稱值中的逗號加上轉義。</span><span class="sxs-lookup"><span data-stu-id="de5e7-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="de5e7-140">產生的字串看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="de5e7-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="de5e7-141">您也可以使用其兩位數的十六進位字元碼來指定該逸出字元。</span><span class="sxs-lookup"><span data-stu-id="de5e7-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="de5e7-142">下列範例會顯示這一點。</span><span class="sxs-lookup"><span data-stu-id="de5e7-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="de5e7-143">不可列印的字元（例如換行字元和換行字元）必須由其兩位數的十六進位字元碼進行轉義和指定。</span><span class="sxs-lookup"><span data-stu-id="de5e7-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="de5e7-144">下列範例會顯示這一點。</span><span class="sxs-lookup"><span data-stu-id="de5e7-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="de5e7-145">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="de5e7-145">For More Information</span></span>

<span data-ttu-id="de5e7-146">如需符合 LDAP 標準之目錄服務所使用之辨別名稱標記法的詳細資訊，請參閱 [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) 。</span><span class="sxs-lookup"><span data-stu-id="de5e7-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 