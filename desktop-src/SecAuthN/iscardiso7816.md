---
description: ISCardISO7816 介面提供執行 ISO 7816-4 功能的方法。
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: 'ISCardISO7816 介面 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 09e5dc9e84a36148e240e4ba2d31f04216454994
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692936"
---
# <a name="iscardiso7816-interface"></a>ISCardISO7816 介面

\[**ISCardISO7816** 介面可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCardISO7816** 介面提供執行 ISO 7816-4 功能的方法。 除了 [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)之外，這些方法會建立封裝于 [**ISCardCmd**](iscardcmd.md)物件中的 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令。

ISO 7816-4 規格定義了 [*智慧卡*](../secgloss/s-gly.md)上可用的標準命令。 此規格也定義了智慧卡 APDU 命令的建立方式，以及如何將它傳送至智慧卡以執行。 此介面會將建立程式自動化。

下列範例顯示 **ISCardISO7816** 介面的一般用法。 在此情況下， **ISCardISO7816** 介面會用來建立 APDU 命令。

**將交易提交至特定卡片**

1.  建立 **ISCardISO7816** 和 [**ISCardCmd**](iscardcmd.md) 介面。

    [**ISCardCmd**](iscardcmd.md)介面是用來封裝 APDU。

2.  呼叫 **ISCardISO7816** 介面的適當方法，並傳遞必要的參數和 [**ISCardCmd**](iscardcmd.md) 介面指標。

    ISO 7816-4 APDU 命令將會建立並封裝在 [**ISCardCmd**](iscardcmd.md) 介面中。

3.  釋放 **ISCardISO7816** 和 [**ISCardCmd**](iscardcmd.md) 介面。

> [!Note]  
> 在 [方法參考] 頁面中，如果未定義資料表中的位序列，則會假設該位序列已保留供日後使用或專屬給特定的供應商使用。

 

## <a name="members"></a>成員

**ISCardISO7816** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardISO7816** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardISO7816** 介面具有這些方法。



| 方法                                                             | 描述                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | 建立命令，以將記錄附加到基本檔 (EF) 的結尾。<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | 從指定的位移開始，依序將 EF 的部分內容設定為其邏輯清除狀態。<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | 根據卡片先前發出的挑戰，有條件地使用卡片計算的結果來更新安全性狀態 (例如，這些 INS 會 \_ 取得 \_ 挑戰命令) 、可能儲存在卡片中的秘密金鑰，以及介面裝置所傳送的驗證資料。<br/> |
| [**GetChallenge**](iscardiso7816-getchallenge.md)                 | 需要發出在安全性相關程式中使用的挑戰。<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | 根據指定的檔案類型，抓取一個基本資料物件或一組包含在結構化資料物件中的資料物件。<br/>                                                                                                                                                          |
| [**GetResponse**](iscardiso7816-getresponse.md)                   | 從卡片傳輸至介面裝置 Apdu，否則無法由可用的通訊協定傳輸。<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | 使用從介面裝置傳送的挑戰資料和儲存在卡片中的相關密碼，來起始卡片的驗證資料的計算。<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | 開啟並關閉邏輯通道。<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | 在目前的 [*資源管理員內容*](../secgloss/r-gly.md)中，儲存一個基本資料物件，或一個或多個包含在結構化資料物件中的資料物件。<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | 建立命令，此命令會取得回應訊息，以提供具有透明結構之 EF 內容的一部分。<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | 會建立一個命令，以讀取基本檔案的指定記錄內容。<br/>                                                                                                                                                                                                            |
| [**SelectFile**](iscardiso7816-selectfile.md)                     | 在邏輯通道中設定目前的檔案。<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | 指派標準類別識別碼位元組，此位元組將在建立 ISO 7816-4 命令 APDU 時用於所有作業中。<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | 使用命令 APDU 中提供的位，起始 EF 中已經存在的位更新。<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | 建立命令，此命令會起始特定記錄的更新。<br/>                                                                                                                                                                                                                                  |
| [**驗證**](iscardiso7816-verify.md)                             | 使用卡片中儲存的參考資料，在從介面裝置傳送的驗證數據卡中起始比較。<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | 起始將二進位值寫入至 EF 的程式。<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | 建立可寫入記錄的命令。<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardsrv .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



 

 
