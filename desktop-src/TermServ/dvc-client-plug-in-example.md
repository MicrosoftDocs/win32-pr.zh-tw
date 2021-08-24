---
title: DVC 用戶端外掛程式範例
description: C + + 程式碼範例，說明如何) 用戶端動態虛擬通道 (DVC) 外掛程式建立遠端桌面連線 (RDC。
ms.assetid: ecc673ec-1bea-4e7c-b1b5-a2342445f6cf
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8b8d79df4156f90c7480296a89685be1bc77f70afb10c3feb2fdded28eff7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285598"
---
# <a name="dvc-client-plug-in-example"></a>DVC 用戶端外掛程式範例

下列 c + + 程式碼範例提供如何) 用戶端動態虛擬通道 (DVC) 外掛程式建立遠端桌面連線 (RDC 的範例。


```C++
/*
 *  Sample "echo" plugin that listens on endpoint "DVC_Sample".
 *
 */
#include "stdafx.h"
#include "resource.h"
#include "DVCPlugin_i.h"
#include <tsvirtualchannels.h>

using namespace ATL;

#define CHECK_QUIT_HR( _x_ )    if(FAILED(hr)) { return hr; }

// CDVCSamplePlugin implements IWTSPlugin.
class ATL_NO_VTABLE CDVCSamplePlugin :
    public CComObjectRootEx<CComMultiThreadModel>,
    public CComCoClass<CDVCSamplePlugin, &CLSID_DVCSamplePlugin>,
    public IWTSPlugin
{
public:

    DECLARE_REGISTRY_RESOURCEID(IDR_PLUGIN)

    BEGIN_COM_MAP(CDVCSamplePlugin)
        COM_INTERFACE_ENTRY(IWTSPlugin)
    END_COM_MAP()

    DECLARE_PROTECT_FINAL_CONSTRUCT()

    HRESULT FinalConstruct()
    {
        return S_OK;
    }

    void FinalRelease()
    {
    }

    // IWTSPlugin.
    //
    HRESULT STDMETHODCALLTYPE
        Initialize(IWTSVirtualChannelManager *pChannelMgr);

    HRESULT STDMETHODCALLTYPE
        Connected() 
    {
        return S_OK; 
    }

    HRESULT STDMETHODCALLTYPE
        Disconnected(DWORD dwDisconnectCode)
    {
        // Prevent C4100 "unreferenced parameter" warnings.
        dwDisconnectCode;

        return S_OK; 
    }

    HRESULT STDMETHODCALLTYPE
        Terminated()
    {
        return S_OK; 
    }

};

OBJECT_ENTRY_AUTO(__uuidof(DVCSamplePlugin), CDVCSamplePlugin)

// CSampleChannelCallback implements IWTSVirtualChannelCallback.
class ATL_NO_VTABLE CSampleChannelCallback :
    public CComObjectRootEx<CComMultiThreadModel>,
    public IWTSVirtualChannelCallback
{
    CComPtr<IWTSVirtualChannel> m_ptrChannel;

public:

    BEGIN_COM_MAP(CSampleChannelCallback)
        COM_INTERFACE_ENTRY(IWTSVirtualChannelCallback)
    END_COM_MAP()

    VOID SetChannel(IWTSVirtualChannel *pChannel)
    {
        m_ptrChannel = pChannel;
    }

    // IWTSVirtualChannelCallback
    //
    HRESULT STDMETHODCALLTYPE
        OnDataReceived(
        ULONG cbSize,
        __in_bcount(cbSize) BYTE *pBuffer
        )
    {
        return m_ptrChannel->Write(cbSize, pBuffer, NULL); 
    }

    HRESULT STDMETHODCALLTYPE
        OnClose()
    { 
        return m_ptrChannel->Close(); 
    }
};


// CSampleListenerCallback implements IWTSListenerCallback.
class ATL_NO_VTABLE CSampleListenerCallback :
    public CComObjectRootEx<CComMultiThreadModel>,
    public IWTSListenerCallback
{
public:

    BEGIN_COM_MAP(CSampleListenerCallback)
        COM_INTERFACE_ENTRY(IWTSListenerCallback)
    END_COM_MAP()

    HRESULT STDMETHODCALLTYPE
        OnNewChannelConnection(
        __in IWTSVirtualChannel *pChannel,
        __in_opt BSTR data,
        __out BOOL *pbAccept,
        __out IWTSVirtualChannelCallback **ppCallback );
};

// IWTSPlugin::Initialize implementation.
HRESULT
    CDVCSamplePlugin::Initialize(
    __in IWTSVirtualChannelManager *pChannelMgr
    )
{
    HRESULT hr; 
    CComObject<CSampleListenerCallback> *pListenerCallback;
    CComPtr<CSampleListenerCallback> ptrListenerCallback;
    CComPtr<IWTSListener> ptrListener;

    // Create an instance of the CSampleListenerCallback object.
    hr = CComObject<CSampleListenerCallback>::CreateInstance(&pListenerCallback);
    CHECK_QUIT_HR("CSampleListenerCallback::CreateInstance");
    ptrListenerCallback = pListenerCallback;

    // Attach the callback to the "DVC_Sample" endpoint.
    hr = pChannelMgr->CreateListener( 
        "DVC_Sample", 
        0, 
        (CSampleListenerCallback*)ptrListenerCallback, 
        &ptrListener);
    CHECK_QUIT_HR("CreateListener");

    return hr;
}

// IWTSListenerCallback::OnNewChannelConnection implementation.
HRESULT
    CSampleListenerCallback::OnNewChannelConnection(
    __in IWTSVirtualChannel *pChannel,
    __in_opt BSTR data,
    __out BOOL *pbAccept,
    __out IWTSVirtualChannelCallback **ppCallback )
{
    HRESULT hr;
    CComObject<CSampleChannelCallback> *pCallback;
    CComPtr<CSampleChannelCallback> ptrCallback;

    // Prevent C4100 "unreferenced parameter" warnings.
    data;

    *pbAccept = FALSE;

    hr = CComObject<CSampleChannelCallback>::CreateInstance(&pCallback);
    CHECK_QUIT_HR("CSampleChannelCallback::CreateInstance");
    ptrCallback = pCallback;

    ptrCallback->SetChannel(pChannel);

    *ppCallback = ptrCallback;
    (*ppCallback)->AddRef();

    *pbAccept = TRUE;

    return hr;
}

```



 

 




