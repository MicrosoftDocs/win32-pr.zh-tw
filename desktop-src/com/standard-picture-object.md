---
title: 標準圖片物件
description: 標準圖片物件
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933642"
---
# <a name="standard-picture-object"></a>標準圖片物件

標準圖片物件提供 GDI 影像的非語言相關抽象概念：點陣圖、圖示、中繼檔和增強的中繼檔。 就像標準字型物件一樣，系統會提供此物件的標準執行。 其主要介面為 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 和 [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)，後者衍生自 **IDispatch** ，以透過 OLE automation 提供圖片屬性的存取權。 使用 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)建立新的圖片物件。

圖片物件也支援輸出介面 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) ，讓用戶端可以決定圖片屬性變更的時間。 因此，圖片物件也支援 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 和一個 **IPropertyNotifySink** 的連接點。

Picture 物件也支援 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ，讓它可以從 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)實例儲存和載入本身。 在內部使用圖片物件的物件通常會在物件的持續性處理過程中，儲存並載入圖片。 [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)函式會根據資料流程內容簡化圖片物件的建立。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項屬性](control-properties.md)
</dt> </dl>

 

 