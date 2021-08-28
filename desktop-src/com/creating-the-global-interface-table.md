---
title: 建立全域介面資料表
description: 建立全域介面資料表
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836cc5507ac9b8e7cccd6e9dc8fd8c2d71e1a23419945ecc01d35b3978940124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793768"
---
# <a name="creating-the-global-interface-table"></a>建立全域介面資料表

使用下列呼叫來建立全域介面資料表物件，並取得 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)的指標：

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> 使用上述呼叫來建立全域介面資料表物件時，必須連結至程式庫 uuid。 這將解析外部符號 CLSID \_ StdGlobalInterfaceTable 和 IID \_ IGlobalInterfaceTable。

 

每個進程都有一個全域介面表的單一實例，因此在處理常式中對這個函式的所有呼叫都會傳回相同的實例。

呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函式之後，請使用 [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) 方法的呼叫，從它所在的單元註冊介面。 這個方法會提供識別介面及其位置的 cookie。 尋找這個介面指標的一個單元會使用此 cookie 來呼叫 [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) 方法，然後執行會提供指向呼叫的單元介面指標。 若要撤銷介面的全域註冊，任何一個單元都可以呼叫 [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) 方法。

使用 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 的簡單範例是當您想要在單一執行緒的單元中將介面指標傳遞 (STA) 至另一個單元中的背景工作執行緒時。 **IGlobalInterfaceTable** 可讓您只傳遞 cookie，而不需要將它封送處理為數據流，並將資料流程以執行緒參數形式傳遞給背景工作執行緒。

當您在全域介面資料表中註冊介面時，您會取得可用的 cookie，而不是在每次需要將指標傳遞至另一個單元 (的 nonmethod 參數，而不是傳遞真正的 (指標) ，也就是要傳遞至另一個單元的 [*參數，以透過*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) 或可在您的部門以外存取的同進程記憶體。

需要注意的原因是，使用全域介面會讓程式設計人員管理問題（例如競爭條件和相互排除）產生額外的負擔，這些問題與從多個執行緒同時存取全域狀態相關聯。

COM 提供 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 介面的標準實作為。 強烈建議您使用這個標準實作為，因為它提供完整的執行緒安全功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用全域介面資料表的時機](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 