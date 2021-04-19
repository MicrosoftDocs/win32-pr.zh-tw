---
description: 用來作為 CryptoAPI 密碼編譯服務提供者的控制碼， (CSP) 或 CNG CSP。
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: 'HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988929"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="74d36-103">HCRYPTPROV \_ 或 \_ NCRYPT \_ 金鑰 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="74d36-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="74d36-104">**HCRYPTPROV \_ 或 NCRYPT \_ 索引 \_ 鍵 \_ 控制碼** 資料類型是用來作為 CryptoAPI [*密碼編譯服務提供者*](../secgloss/c-gly.md)的控制碼， (CSP) 或 CNG csp。</span><span class="sxs-lookup"><span data-stu-id="74d36-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="74d36-105">這個控制碼必須是使用 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)函式所建立的 [**HCRYPTPROV**](hcryptprov.md)控制碼，或使用 [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey)函式建立的 **NCRYPT 索引 \_ 鍵 \_ 控制碼** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="74d36-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="74d36-106">新的應用程式應該一律將 **NCRYPT \_ 金鑰 \_ 控制碼** 控制碼傳入 CNG CSP。</span><span class="sxs-lookup"><span data-stu-id="74d36-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="74d36-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="74d36-107">Requirements</span></span>



| <span data-ttu-id="74d36-108">需求</span><span class="sxs-lookup"><span data-stu-id="74d36-108">Requirement</span></span> | <span data-ttu-id="74d36-109">值</span><span class="sxs-lookup"><span data-stu-id="74d36-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74d36-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74d36-110">Minimum supported client</span></span><br/> | <span data-ttu-id="74d36-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74d36-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74d36-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74d36-112">Minimum supported server</span></span><br/> | <span data-ttu-id="74d36-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74d36-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74d36-114">標頭</span><span class="sxs-lookup"><span data-stu-id="74d36-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d36-115"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="74d36-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
