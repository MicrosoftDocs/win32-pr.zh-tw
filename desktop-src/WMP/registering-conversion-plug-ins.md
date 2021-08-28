---
title: 註冊轉換外掛程式
description: 註冊轉換外掛程式
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player，轉換外掛程式
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，註冊
- 登錄，轉換外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e6741a27c665b8a99cda2c756fa28cbdbb16f92564f26c16e077c5c5be8859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861538"
---
# <a name="registering-conversion-plug-ins"></a>註冊轉換外掛程式

必須先註冊協力廠商格式，Windows Media Player 才能具現化並使用轉換外掛程式。 若要註冊您的檔案以進行轉換，您必須註冊與您的格式相關聯的副檔名。

已註冊的副檔名清單會以一組登錄機碼的形式來保存。 如需註冊協力廠商格式的詳細資訊，請參閱副檔名登錄[設定](file-name-extension-registry-settings.md)。 下表列出登錄值設定，以註冊協力廠商格式以使用轉換外掛程式進行轉換。



| 值                  | 設定                                                     |
|------------------------|-------------------------------------------------------------|
| **執行階段**            | 13                                                          |
| **權限**        | 8 (程式庫) 的許可權。                             |
| **ConvertPluginCLSID** | 轉換外掛程式的類別識別碼，以登錄格式為。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**轉換外掛程式程式設計參考**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




