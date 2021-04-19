---
description: 將私密金鑰和其對應的公開金鑰儲存至指定的檔案。
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988896"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="1b3d7-103">PvkPrivateKeySave 函式</span><span class="sxs-lookup"><span data-stu-id="1b3d7-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b3d7-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-104">This API is deprecated.</span></span> <span data-ttu-id="1b3d7-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="1b3d7-106">**PvkPrivateKeySave** 函式會將 [*私密金鑰*](../secgloss/p-gly.md)和其對應的 [*公開金鑰*](../secgloss/p-gly.md)儲存至指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="1b3d7-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="1b3d7-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1b3d7-109">語法</span><span class="sxs-lookup"><span data-stu-id="1b3d7-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1b3d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b3d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b3d7-111">*hCryptProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3d7-112">[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="1b3d7-113">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3d7-114">以初始讀取/寫入權限和後續唯讀許可權建立之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d7-115">*dwKeySpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3d7-116">索引鍵類型的長整數。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-116">A long integer for the type of key.</span></span> <span data-ttu-id="1b3d7-117">可能的值包括 **在 \_ KEYEXCHANGE** **或簽 \_** 章。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d7-118">*hwndOwner* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3d7-119">如果需要密碼來加密私密金鑰，此參數是對話方塊父系的控制碼;否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d7-120">*pwszKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3d7-121">要儲存的索引鍵名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d7-122">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3d7-123">指定函數其他選項的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="1b3d7-124">如需詳細資訊，請參閱 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)中的 *dwFlags* 參數。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b3d7-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b3d7-125">Return value</span></span>

<span data-ttu-id="1b3d7-126">成功時，此函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="1b3d7-127">如果失敗， **PvkPrivateKeySave** 函數會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1b3d7-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3d7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b3d7-128">Requirements</span></span>



| <span data-ttu-id="1b3d7-129">需求</span><span class="sxs-lookup"><span data-stu-id="1b3d7-129">Requirement</span></span> | <span data-ttu-id="1b3d7-130">值</span><span class="sxs-lookup"><span data-stu-id="1b3d7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3d7-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b3d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1b3d7-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1b3d7-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b3d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1b3d7-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b3d7-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b3d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1b3d7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b3d7-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b3d7-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
