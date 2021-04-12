---
description: 當應用程式在任何可寫入的 Windows 映像取得 (WIA) 屬性上執行 IPropertyStorage：： WriteMultiple 作業時，WIA 驅動程式會在新的屬性值上執行驗證。
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: WIA 屬性驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191384"
---
# <a name="wia-property-validation"></a>WIA 屬性驗證

當應用程式在任何可寫入的 Windows 映像取得 (WIA) 屬性上執行 [IPropertyStorage：： WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) 作業時，wia 驅動程式會在新的屬性值上執行驗證。 寫入一個屬性可能會影響變更其他屬性值的副作用。 在寫入作業之後，應用程式會讀取所有屬性值，以判斷所有屬性都設定為應用程式所需的值。

您可以使用 [IPropertyStorage：： WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) 作業同時寫入多個屬性。 在某些情況下，某些屬性指派會發生衝突。 在這種情況下，用來解決衝突的優先順序如下所示：

1.  WIA \_ IP 的 \_ 當前 \_ 意圖
2.  WIA \_ IPA \_ 資料類型
3.  WIA \_ IPA \_ 深度
4.  WIA \_ IP \_ XRES
5.  WIA \_ IP \_ YRES
6.  WIA \_ IP \_ XPOS
7.  WIA \_ IP \_ YPOS
8.  WIA \_ IP \_ 範圍
9.  WIA \_ IP \_ YEXTENT

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
