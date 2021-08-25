---
title: CLSID 金鑰
description: CLSID 是識別 COM 類別物件的全域唯一識別碼。 如果您的伺服器或容器允許連結至其内嵌物件，您必須為每個支援的物件類別註冊 CLSID。
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CLSID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd390fc6a1ccb15e128245c3b6a80e2b4ca57f41de9e9c21e93ebe4c708783d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854978"
---
# <a name="clsid-key"></a>CLSID 金鑰

CLSID 是識別 COM 類別物件的全域唯一識別碼。 如果您的伺服器或容器允許連結至其内嵌物件，您必須為每個支援的物件類別註冊 CLSID。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID** \\ *{* CLSID *}*



| 登錄機碼                                                 | 說明                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid.md)                                       | 將 AppID 與 CLSID 相關聯。                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | 指定將物件的指定類別自動轉換成物件的新類別。                                                |
| [**AutoTreatAs**](autotreatas.md)                           | 自動將 [**TreatAs**](treatas.md) 索引鍵的 CLSID 設定為指定的值。                                              |
| [**AuxUserType**](auxusertype.md)                           | 指定應用程式的簡短顯示名稱和應用程式名稱。                                                                     |
| [**控制**](control.md)                                   | 將物件識別為 ActiveX 控制項。                                                                                              |
| [**轉換**](conversion.md)                             | 由 [ **轉換** ] 對話方塊用來判斷應用程式可以讀取和寫入的格式。                                           |
| [**DataFormats**](dataformats.md)                           | 指定應用程式所支援的預設和主要資料格式。                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | 提供 iconic 物件簡報的預設圖示資訊。                                                                   |
| [**InprocHandler**](inprochandler.md)                       | 指定應用程式是否使用自訂處理常式。                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | 指定應用程式是否使用自訂處理常式。                                                                                  |
| [**InprocServer**](inprocserver.md)                         | 指定同進程伺服器 DLL 的路徑。                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | 註冊32位的同進程伺服器，並指定伺服器可以在其中執行之單元的執行緒模型。                           |
| [**插入**](insertable.md)                             | 指出當 COM 容器應用程式使用時，這個類別的物件應該出現在 [ **插入物件** ] 對話方塊清單方塊中。 |
| [**介面**](interface.md)                               | 選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。                                             |
| [**LocalServer**](localserver.md)                           | 指定16位本機伺服器應用程式的完整路徑。                                                                            |
| [**LocalServer32**](localserver32.md)                       | 指定32位本機伺服器應用程式的完整路徑。                                                                            |
| [**MiscStatus**](miscstatus.md)                             | 指定如何建立和顯示物件。                                                                                           |
| [**ProgID**](progid.md)                                     | 將 ProgID 與 CLSID 產生關聯。                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | 識別要用於工具列或工具箱按鈕臉部的 16 x 16 點陣圖的模組名稱和資源識別碼。                      |
| [**TreatAs**](treatas.md)                                   | 指定可模擬目前類別之類別的 CLSID。                                                                       |
| [**動詞命令**](verb.md)                                         | 指定要為應用程式註冊的動詞。                                                                                 |
| [**版本**](version.md)                                   | 指定控制項的版本號碼。                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | 將 ProgID 與 CLSID 產生關聯。 此值可用來判斷物件應用程式的最新版本。                           |



 

## <a name="remarks"></a>備註

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

CLSID 索引鍵包含當類別處於執行中狀態時，預設 COM 處理常式用來傳回其相關資訊的資訊。

若要取得應用程式的 CLSID，您可以使用 Uuidgen.exe，或使用 [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) 函數。

CLSID 是一對大括弧內的128位數位（以十六進位表示）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




