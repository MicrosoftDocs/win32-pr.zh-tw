---
description: 剖析器匯出函數會提供剖析器 DLL 中剖析器的所有功能。 每個剖析器 DLL 都必須執行 ParserAutoInstallInfo 和 DllMain。 其餘的匯出函數必須針對剖析器 DLL 中包含的每個剖析器來執行。
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: 執行剖析器匯出函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e32b3b1aa807a604f058ed8965ef11728f6c12fecb34e27a337682361f8dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778838"
---
# <a name="implementing-parser-export-functions"></a>執行剖析器匯出函數

剖析器匯出函數會提供剖析器 DLL 中剖析器的所有功能。 每個剖析器 DLL 都必須執行 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) 和 [**DllMain**](dllmain-parser.md)。 其餘的匯出函數必須針對剖析器 DLL 中包含的每個剖析器來執行。

下列主題會示範如何執行匯出函數。



| 詞彙                                                                                                                                                                                                                                                   | 描述                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[執行 ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | 提供執行 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) 函式的描述和程式碼範例，該函式會識別位於剖析器 DLL 中的剖析器。<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[執行 DllMain 剖析器](implementing-dllmain-parser.md)<br/>                                    | 提供執行 [**DllMain**](dllmain-parser.md) 剖析器函式的描述和程式碼範例，該函式可識別剖析器是否存在，然後釋放網路監視器用於剖析器的資源。<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[執行註冊](implementing-register.md)<br/>                                                                  | 提供執行 [**Register**](register-parser.md) 函式的描述和程式碼範例，此函數會記錄通訊協定的所有屬性。<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[執行 RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | 提供執行 [**RecognizeFrame**](recognizeframe.md) 函式的描述和程式碼範例，該函式會識別框架中的通訊協定實例。<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[執行 AttachProperties](implementing-attachproperties.md)<br/>                          | 提供執行 [**AttachProperties**](attachproperties.md) 函式的描述和程式碼範例，該函式會分隔剖析器可辨識的資料，然後將屬性描述附加至存在於已辨識資料中的每個通訊協定屬性。<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[執行 FormatProperties](implementing-formatproperties.md)<br/>                          | 提供執行 [**FormatProperties**](formatproperties.md) 函式的描述和程式碼範例，此函式會格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[執行取消註冊](implementing-deregister.md)<br/>                                                        | 提供執行 [**取消註冊函**](deregister.md) 式的描述和程式碼範例，該函式會釋放用來登錄通訊協定屬性的資源。<br/>                                                                                                     |



 

 

 




