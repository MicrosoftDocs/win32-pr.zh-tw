---
title: LaunchPage 方法
description: LaunchPage 方法
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Windows Media Player 外掛程式，LaunchPage 方法
- 外掛程式，LaunchPage 方法
- 使用者介面外掛程式，LaunchPage 方法
- UI 外掛程式，LaunchPage 方法
- LaunchPage 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021659"
---
# <a name="the-launchpage-method"></a>LaunchPage 方法

LaunchPage 方法提供外掛程式的主要功能，也就是啟動搜尋頁面，其中包含傳遞給方法之媒體專案的演出者相關資訊。

OnSearch 方法會使用目前的 **媒體** 物件來呼叫這個方法。

下列程式碼會用來執行此方法：


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




