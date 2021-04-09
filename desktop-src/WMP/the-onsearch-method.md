---
title: OnSearch 方法
description: OnSearch 方法
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Windows Media Player 外掛程式，OnSearch 方法
- 外掛程式，OnSearch 方法
- 使用者介面外掛程式，OnSearch 方法
- UI 外掛程式，OnSearch 方法
- OnSearch 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021557"
---
# <a name="the-onsearch-method"></a>OnSearch 方法

按一下 [ **搜尋** ] 按鈕時，Windows Media Player 會呼叫 OnSearch 方法。 這個方法會抓取目前的 **媒體** 物件，並將它傳遞給 LaunchPage 方法。

下列程式碼會用來執行此方法：


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




