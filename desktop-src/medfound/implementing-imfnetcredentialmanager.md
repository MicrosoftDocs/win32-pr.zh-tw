---
description: 執行 IMFNetCredentialManager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: 執行 IMFNetCredentialManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986363"
---
# <a name="implementing-imfnetcredentialmanager"></a>執行 IMFNetCredentialManager

在 [**IMFNetCredentialManager：： BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) 方法中，執行下列動作。

1.  如果您還沒有 [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) 指標，請呼叫 [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) 來建立認證快取物件。 儲存此指標。
2.  呼叫 [**IMFNetCredentialCache：： GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)。 在 *dwAuthenticationFlags* 參數中設定旗標，如下所示：
    -   如果 [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam)結構的 **HrOp** 成員等於 **NS \_ E \_ proxy \_ ACCESSDENIED**，請設定 **MFNET \_ AUTHENTICATION \_ PROXY** 旗標。
    -   如果 **fClearTextPackage** 為 **TRUE**，請設定 **MFNET \_ AUTHENTICATION \_ 純 \_ 文本** 旗標。
    -   如果 **fAllowLoggedOnUser** 為 **TRUE**，請設定 **\_ \_ 登入 \_ \_ 使用者** 旗標的 MFNET AUTHENTICATION。
3.  [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential)方法會傳回 [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential)指標，可能需要 \_ 提示旗標。 儲存 **IMFNetCredential** 指標。
4.  如果 [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 未傳回「 **需要 \_ 提示** 」旗標，則您已完成。 跳至步驟9。
5.  否則，如果 [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) 傳回「 **需要 \_ 提示** 」旗標，您必須提示使用者輸入其使用者名稱和密碼。
6.  如果 **fClearTextPackage** 為 **FALSE**，請加密認證。
7.  呼叫 [**IMFNetCredential：： SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) 和 [**IMFNetCredential：： SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) ，以設定認證物件上的使用者名稱和密碼。
8.  （選擇性）呼叫 [**IMFNetCredentialCache：： SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) ，以使用者的儲存和傳送認證的喜好設定來更新認證快取物件。
9.  藉由呼叫 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)來叫用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)回呼。

在 [**IMFNetCredentialManager：： EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials)方法中，傳回 [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)方法中取得的 [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential)指標。

在 [**IMFNetCredentialManager：： SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) 方法中，將輸入參數直接傳遞給 [**IMFNetCredentialCache：： SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) 方法。 這會通知認證快取伺服器是否接受認證。

如果您需要提示使用者 (步驟 5) 或加密 (步驟 6) 的認證，您應該在工作佇列執行緒上這麼做，如此您就不會封鎖 Microsoft 媒體基礎管線。 呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ，然後執行工作佇列回呼內的其餘步驟。

> [!Note]  
> 請注意，在建立網路來源時，可能會叫用 [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) 。 因此，如果您藉由呼叫同步 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 方法來建立網路來源，則在取得認證時，呼叫的執行緒可能會封鎖。 因此，建議您改用非同步 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) 方法。

 

## <a name="example"></a>範例

此範例顯示一個認證管理員可以提供的行為類型。

以下是實 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)的類別宣告。


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



若要追蹤 [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) 作業的狀態，類別會使用下列 helper 物件：


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



[**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)方法會建立認證快取，並取得 [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential)指標。 如果使用者必須收到提示 (由 [ **需要 \_ 提示** ] 旗標表示) ，方法會呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 來將新的工作專案排入佇列：


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



工作佇列執行緒會呼叫 [**invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)，這會提示使用者，然後呼叫 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) 來叫用 [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)中提供的回呼指標。


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



[**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials)方法會將 [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential)指標傳回呼叫端，以完成作業。


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路來源驗證](network-source-authentication.md)
</dt> </dl>

 

 



