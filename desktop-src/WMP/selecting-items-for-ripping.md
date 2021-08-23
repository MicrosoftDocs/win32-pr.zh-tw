---
title: 選取要進行翻錄的專案
description: 選取要進行翻錄的專案
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media PlayerMobile ActiveX control、CD 翻錄
- Windows Media Player行動電話、CD 翻錄
- CD 翻錄，選取專案
- 將 Cd 翻錄，選取專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea677028fab6b3c39466e916bd8bb59ea8cee4d370730c096cbb98978f4abc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646648"
---
# <a name="selecting-items-for-ripping"></a>選取要進行翻錄的專案

有時候使用者不會想要在 CD 上翻錄每個曲目。 Windows Media Player 提供介面來指定要針對翻錄選取的追蹤。 通常在 CD 翻錄應用程式中有一個使用者介面，可讓使用者在 CD 的曲目清單中選取核取方塊。

預設可能不會針對翻錄選取某些曲目。 如果 Windows Media Player 程式庫中已經有一個曲目，它就不會自動選取以進行翻錄。 本節中的第二個程式碼範例會示範如何略過預設值，並在已翻錄的情況下手動選取要進行翻錄的播放軌。

下列程式碼範例示範如何判斷是否已選取要進行翻錄的追蹤：


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



下列程式碼範例示範如何指定是否已選取要進行翻錄的追蹤。


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將 CD 翻錄**](ripping-a-cd.md)
</dt> <dt>

[**擷取轉錄介面**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**啟動 Rip 進程**](starting-the-rip-process.md)
</dt> <dt>

[**正在抓取 Rip 狀態**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




