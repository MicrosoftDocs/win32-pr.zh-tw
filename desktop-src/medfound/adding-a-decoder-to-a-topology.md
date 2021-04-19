---
description: 將解碼器新增至拓撲
ms.assetid: 32c088d5-d9dd-43d3-a63b-219e6a7a36b1
title: 將解碼器新增至拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506963ee65490365b60788808a4da87c21355247
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973054"
---
# <a name="adding-a-decoder-to-a-topology"></a>將解碼器新增至拓撲

本主題說明如何將音訊或影片解碼器新增至拓撲。

針對大部分的播放應用程式，您可以從傳送至媒體會話的部分拓撲中省略這些解碼器。 媒體會話會使用拓撲載入器來完成拓撲，而拓撲載入器會插入所需的任何解碼器。 但是，如果您想要選取特定的解碼器，則可以手動將解碼器加入拓撲中。

以下是將解碼器新增至拓撲的整體步驟。

1.  尋找此解碼器的 CLSID。
2.  在拓撲中新增該解碼器的節點。
3.  若為影片解碼，請啟用 DirectX Video 加速。 音訊解碼器不需要此步驟。

## <a name="find-the-decoder-clsid"></a>尋找解碼器 CLSID

如果您想要使用特定的解碼器，您可能已經知道此解碼器的 CLSID。 若是如此，您可以略過此步驟。 否則，請使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數來查閱登錄中的 CLSID。 此函式會採用數個搜尋準則做為輸入。 若要尋找解碼器，您只需要指定輸入格式 (主要類型和子類型) 。 您可以從資料流程描述項取得這些，如下列程式碼所示。


```C++
// Returns the MFT decoder based on the major type GUID.

HRESULT GetDecoderCategory(const GUID& majorType, GUID *pCategory)
{
    if (majorType == MFMediaType_Video)
    {
        *pCategory = MFT_CATEGORY_VIDEO_DECODER;
    }
    else if (majorType == MFMediaType_Audio)
    {
        *pCategory = MFT_CATEGORY_AUDIO_DECODER;
    }
    else
    {
        return MF_E_INVALIDMEDIATYPE;
    }
    return S_OK;
}

// Finds a decoder for a stream.
//
// If the stream is not compressed, pCLSID receives the value GUID_NULL.

HRESULT FindDecoderForStream(
    IMFStreamDescriptor *pSD,   // Stream descriptor for the stream.
    CLSID *pCLSID               // Receives the CLSID of the decoder.
    )
{
    BOOL    bIsCompressed = FALSE;
    GUID    guidMajorType = GUID_NULL;
    GUID    guidSubtype = GUID_NULL;
    GUID    guidDecoderCategory = GUID_NULL;

    CLSID *pDecoderCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cDecoderCLSIDs = NULL;   // Size of the array.

    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pMediaType = NULL;

    // Find the media type for the stream.
    HRESULT hr = pSD->GetMediaTypeHandler(&pHandler);

    if (SUCCEEDED(hr))
    {
        hr = pHandler->GetCurrentMediaType(&pMediaType);
    }

    // Get the major type and subtype.
    if (SUCCEEDED(hr))
    {
        hr = pMediaType->GetMajorType(&guidMajorType);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMediaType->GetGUID(MF_MT_SUBTYPE, &guidSubtype);
    }

    // Check whether the stream is compressed.
    if (SUCCEEDED(hr))
    {
        hr = pMediaType->IsCompressedFormat(&bIsCompressed);
    }

#if (WINVER < _WIN32_WINNT_WIN7)

    // Starting in Windows 7, you can connect an uncompressed video source 
    // directly to the EVR. In earlier versions of Media Foundation, this
    // is not supported.

    if (SUCCEEDED(hr))
    {
        if (!bIsCompressed && (guidMajorType == MFMediaType_Video))
        {
            hr = MF_E_INVALIDMEDIATYPE;
        }
    }
#endif

    // If the stream is compressed, find a decoder.
    if (SUCCEEDED(hr))
    {
        if (bIsCompressed)
        {
            // Select the decoder category from the major type (audio/video).
            hr = GetDecoderCategory(guidMajorType, &guidDecoderCategory);

            // Look for a decoder.

            if (SUCCEEDED(hr))
            {
                MFT_REGISTER_TYPE_INFO tinfo;
                tinfo.guidMajorType = guidMajorType;
                tinfo.guidSubtype = guidSubtype;

                hr = MFTEnum(
                        guidDecoderCategory,
                        0,               // Reserved
                        &tinfo,          // Input type to match. (Encoded type.)
                        NULL,            // Output type to match. (Don't care.)
                        NULL,            // Attributes to match. (None.)
                        &pDecoderCLSIDs, // Receives a pointer to an array of CLSIDs.
                        &cDecoderCLSIDs  // Receives the size of the array.
                        );
            }

            // MFTEnum can return zero matches.
            if (SUCCEEDED(hr) && (cDecoderCLSIDs == 0))
            {
                hr = MF_E_TOPO_CODEC_NOT_FOUND;
            }

            // Return the first CLSID in the list to the caller.
            if (SUCCEEDED(hr))
            {
                *pCLSID = pDecoderCLSIDs[0];
            }
        }
        else
        {
            // Uncompressed. A decoder is not required.
            *pCLSID = GUID_NULL;
        }
    }

    SafeRelease(&pHandler);
    SafeRelease(&pMediaType);
    CoTaskMemFree(pDecoderCLSIDs);

    return hr;
}
```



如需資料流程描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)函式會傳回 clsid 陣列的指標。 傳回陣列的順序是任意的。 在此範例中，函數會使用陣列中的第一個 CLSID。 您可以呼叫 [**MFTGetInfo**](/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo)，以取得更多關於解碼器的資訊，包括該解碼器的易記名稱。 此外，請注意， **MFTEnum** 可以成功，但會傳回空的陣列，因此請務必檢查在最後一個參數中傳回的陣列大小。

## <a name="add-the-decoder-node-to-the-topology"></a>將解碼器節點新增至拓撲

當您擁有該解碼器的 CLSID 之後，請呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)來建立新的轉換節點。 在節點上設定 [ [**MF \_ TOPONODE \_ 轉換 \_ OBJECTID**](mf-toponode-transform-objectid-attribute.md) ] 屬性，以指定 CLSID。 如需如何建立轉換節點的範例，請參閱 [建立轉換](creating-transform-nodes.md)節點。 然後藉由呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput)，將來源節點連接至「解碼器」節點，並將「解碼」節點連接至輸出節點。

下列範例示範如何建立節點並加以連接。 此範例與名為的範例函式非常類似， `AddBranchToPartialTopology` 它會在 [建立播放拓撲](creating-playback-topologies.md)的主題中顯示。 唯一的差別在於，此範例會為該解碼器新增額外的節點。


```C++
HRESULT AddBranchToPartialTopologyWithDecoder(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd                  // Window for video playback.
    )
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;
    IMFTopologyNode     *pDecoderNode = NULL;

    BOOL fSelected = FALSE;
    CLSID clsidDecoder = GUID_NULL;

    // Get the stream descriptor.
    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        return hr;
    }

    if (fSelected)
    {
        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);

        // Create the media sink activation object.
        if (SUCCEEDED(hr))
        {
            hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        }

        // Create the output node for the renderer.
        if (SUCCEEDED(hr))
        {
            hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        }

        // Find a decoder.
        if (SUCCEEDED(hr))
        {
            hr = FindDecoderForStream(pSD, &clsidDecoder);
        }

        if (SUCCEEDED(hr))
        {
            if (clsidDecoder == GUID_NULL)
            {
                // No decoder is required. 
                // Connect the source node to the output node.
                hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
            }
            else
            {
                // Add a decoder node.
                hr = AddTransformNode(pTopology, clsidDecoder, &pDecoderNode);

                // Connect the source node to the decoder node.
                if (SUCCEEDED(hr))
                {
                    hr = pSourceNode->ConnectOutput(0, pDecoderNode, 0);
                }

                // Connect the decoder node to the output node.
                if (SUCCEEDED(hr))
                {
                    hr = pDecoderNode->ConnectOutput(0, pOutputNode, 0);
                }
            }
        }

        // Mark this branch as not requiring a decoder.
        if (SUCCEEDED(hr))
        {
            hr = pOutputNode->SetUINT32(
                MF_TOPONODE_CONNECT_METHOD, 
                MF_CONNECT_ALLOW_CONVERTER
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pDecoderNode->SetUINT32(
                MF_TOPONODE_CONNECT_METHOD, 
                MF_CONNECT_ALLOW_CONVERTER
                );
        }

    }
    // else: If not selected, don't add the branch. 

    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pDecoderNode);

    return hr;
}
```



## <a name="enable-video-acceleration"></a>啟用影片加速

將音訊或影片解碼器新增至拓撲的下一個步驟僅適用于影片解碼器。 若要取得影片播放的最佳效能，您應該啟用 DirectX Video 加速 (DXVA) 如果影片解碼支援此功能。 此步驟通常是由拓撲載入器執行，但如果您手動將此解碼器新增至拓撲，您必須自行執行此步驟。

作為此步驟的先決條件，拓撲中的所有輸出節點都必須系結至媒體接收器。 如需詳細資訊，請參閱 [將輸出節點系結至媒體接收器](binding-output-nodes-to-media-sinks.md)。

首先，在拓撲中尋找裝載 Direct3D 裝置管理員的物件。 若要這樣做，請從每個節點取得物件指標，然後查詢 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 服務的物件。 一般而言，增強型影片轉譯器 (EVR) 為此角色提供服務。 下列程式碼顯示的函式會尋找裝置管理員：


```C++
// Finds the node in the topology that provides the Direct3D device manager. 

HRESULT FindDeviceManager(
    IMFTopology *pTopology,         // Topology to search.
    IUnknown **ppDeviceManager,     // Receives a pointer to the device manager.
    IMFTopologyNode **ppNode        // Receives a pointer to the node.
    )
{
    HRESULT hr = S_OK;
    WORD cNodes = 0;
    BOOL bFound = FALSE;

    IMFTopologyNode *pNode = NULL;
    IUnknown *pNodeObject = NULL;
    IDirect3DDeviceManager9 *pD3DManager = NULL;

    // Search all of the nodes in the topology.
    
    hr = pTopology->GetNodeCount(&cNodes);

    if (FAILED(hr))
    {
        return hr;
    }

    for (WORD i = 0; i < cNodes; i++)
    {
        // For each of the following calls, failure just means we 
        // did not find the node we're looking for, so keep looking. 

        hr = pTopology->GetNode(i, &pNode);

        // Get the node's object pointer.
        if (SUCCEEDED(hr))
        {
            hr = pNode->GetObject(&pNodeObject);
        }

        // Query the node object for the device manager service.
        if (SUCCEEDED(hr))
        {
            hr = MFGetService(
                pNodeObject, 
                MR_VIDEO_ACCELERATION_SERVICE, 
                IID_PPV_ARGS(&pD3DManager)
                );
        }

        if (SUCCEEDED(hr))
        {
            // Found the right node. Return the pointers to the caller.
            *ppDeviceManager = pD3DManager;
            (*ppDeviceManager)->AddRef();

            *ppNode = pNode;
            (*ppNode)->AddRef();

            bFound = TRUE;
            break;
        }

        SafeRelease(&pNodeObject);
        SafeRelease(&pD3DManager);
        SafeRelease(&pNode);

    } // End of for loop.

    SafeRelease(&pNodeObject);
    SafeRelease(&pD3DManager);
    SafeRelease(&pNode);

    return bFound ? S_OK : E_FAIL;
}
```



接下來，從包含 Direct3D 裝置管理員的節點中，尋找直接上游的轉換節點。 從這個轉換節點取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標。 **IMFTransform** 指標代表媒體基礎轉換 (MFT) 。 視節點的建立方式而定，您可能需要呼叫 **CoCreateInstance** 來建立 mft，或從啟用物件啟動 mft。 下列程式碼會處理所有的各種案例：


```C++
// Returns the MFT for a transform node.

HRESULT GetTransformFromNode(
    IMFTopologyNode *pNode, 
    IMFTransform **ppMFT
    )
{
    MF_TOPOLOGY_TYPE type = MF_TOPOLOGY_MAX;

    IUnknown *pNodeObject = NULL;
    IMFTransform *pMFT = NULL;
    IMFActivate *pActivate = NULL;
    IMFAttributes *pAttributes = NULL;

    // Is this a transform node?
    HRESULT hr = pNode->GetNodeType(&type);

    if (FAILED(hr))
    {
        return hr;
    }

    if (type != MF_TOPOLOGY_TRANSFORM_NODE)
    {
        // Wrong node type.
        return E_FAIL;
    }

    // Check whether the node has an object pointer.
    hr = pNode->GetObject(&pNodeObject);

    if (SUCCEEDED(hr))
    {
        // The object pointer should be one of the following:
        // 1. Pointer to an MFT.
        // 2. Pointer to an activation object.

        // Is it an MFT? Query for IMFTransform.
        hr = pNodeObject->QueryInterface(IID_IMFTransform, (void**)&pMFT);
        if (FAILED(hr))
        {
            // It is not an MFT, so it should be an activation object.
            hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

            // Use the activation object to create the MFT.

            if (SUCCEEDED(hr))
            {
                hr = pActivate->ActivateObject(IID_PPV_ARGS(&pMFT));
            }

            // Replace the node's object pointer with the MFT.
            if (SUCCEEDED(hr))
            {
                hr = pNode->SetObject(pMFT);
            }

            // If the activation object has the MF_ACTIVATE_MFT_LOCKED 
            // attribute, transfer this value to the
            // MF_TOPONODE_MFT_LOCKED attribute on the node.
            // However, don't fail if this attribute is not found.
            if (SUCCEEDED(hr))
            {
                BOOL bLocked = MFGetAttributeUINT32(
                    pActivate, MF_ACTIVATE_MFT_LOCKED, FALSE);


                hr = pNode->SetUINT32(MF_TOPONODE_LOCKED, bLocked);
            }
        }
    }
    else
    {
        GUID clsidMFT;

        // The node does not have an object pointer. Look for a CLSID.
        hr = pNode->GetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, &clsidMFT);
       
        // Create the MFT.
        if (SUCCEEDED(hr))
        {
            hr = CoCreateInstance(
                clsidMFT, NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pMFT)
                );
        }

        // If the MFT supports attributes, copy the node attributes to the 
        // MFT attribute store. 
        if (SUCCEEDED(hr))
        {
            if (SUCCEEDED(pMFT->GetAttributes(&pAttributes)))
            {
                // Copy from pNode to pAttributes.
                hr = pNode->CopyAllItems(pAttributes); 
            }
        }

        // Set the object on the node.
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pMFT);
        }
    }

    // Return the IMFTransform pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pMFT);
    SafeRelease(&pActivate);
    SafeRelease(&pAttributes);
    return hr;
}
```



如果 MFT 具有具有值 **TRUE** 的 [**MF \_ SA \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)屬性，則表示此 mft 支援 DirectX Video 加速。 下列函數會測試此屬性：


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



若要在此 MFT 上啟用影片加速[](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) ，請使用 mft \_ 訊息 \_ 集 \_ D3D \_ 管理員訊息來呼叫 IMFTransform：:P rocessmessage。 也請在 [轉換] 節點上，將 [ [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md) ] 屬性設定為 [ **TRUE** ]。 這個屬性會通知管線已啟用影片加速。 下列程式碼會執行這些步驟：


```C++
// Enables or disables DirectX Video Acceleration in a topology.

HRESULT EnableVideoAcceleration(IMFTopology *pTopology, BOOL bEnable)
{
    IMFTopologyNode *pD3DManagerNode = NULL;
    IMFTopologyNode *pUpstreamNode = NULL;
    IUnknown *pD3DManager = NULL;
    IMFTransform *pMFT = NULL;

    // Look for the node that supports the Direct3D Manager.
    
    HRESULT hr = FindDeviceManager(pTopology, &pD3DManager, &pD3DManagerNode); 
    if (FAILED(hr))
    {
        //  There is no Direct3D device manager in the topology.
        //  This is not a failure case.
        return S_OK;
    }

    DWORD dwOutputIndex = 0;

    // Get the node upstream from the device manager node.
    hr = pD3DManagerNode->GetInput(0, &pUpstreamNode, &dwOutputIndex);

    // Get the MFT from the upstream node.
    if (SUCCEEDED(hr))
    {
        hr = GetTransformFromNode(pUpstreamNode, &pMFT);
    }

    // If the MFT is Direct3D-aware, notify the MFT of the device 
    // manager and mark the topology node as Direct3D-aware.
    if (SUCCEEDED(hr))
    {
        if (IsTransformD3DAware(pMFT))
        {
            ULONG_PTR ptr = bEnable ? (ULONG_PTR)pD3DManager : NULL;

            hr = pMFT->ProcessMessage(MFT_MESSAGE_SET_D3D_MANAGER, ptr);

            // Mark the node.
            if (SUCCEEDED(hr))
            {
                hr = pUpstreamNode->SetUINT32(MF_TOPONODE_D3DAWARE, bEnable);
            }
        }
    }

    SafeRelease(&pD3DManagerNode);
    SafeRelease(&pUpstreamNode);
    SafeRelease(&pD3DManager);
    SafeRelease(&pMFT);
    return hr;
}
```



如需媒體基礎中 DXVA 的詳細資訊，請參閱 [DirectX Video 加速 2.0](directx-video-acceleration-2-0.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 拓朴建築](advanced-topology-building.md)
</dt> </dl>

 

 



