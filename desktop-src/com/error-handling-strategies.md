---
title: 錯誤處理策略
description: 錯誤處理策略
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c594a8b1e5baf0eab3d928b8f1b861b7f0160d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104462692"
---
# <a name="error-handling-strategies"></a>錯誤處理策略

因為介面方法是虛擬的，所以呼叫端不可能知道任何一個呼叫可能傳回的一組完整值。 方法的一種實值可能會傳回五個值;另一個可能會傳回八個。

檔會列出每個方法可能傳回的常見值;這些是您必須在程式碼中檢查和處理的值，因為它們具有特殊意義。 可能會傳回其他值，但因為它們沒有意義，所以您不需要撰寫特殊的程式碼來處理它們。 零或非零的簡單檢查即已足夠。

## <a name="hresult-values"></a>HRESULT 值

COM 函數和方法的傳回值是 **HRESULT**。 某些 Hresult 的值已在 COM 中變更，以消除所有重複和與系統錯誤碼重迭的情況。 重複系統錯誤碼的系統已變更為 [設備 \_ WIN32]，而重迭的則會保留在設備 \_ Null 中。 下表列出常見的 **HRESULT** 值和其值。



| HRESULT                    | 值                 | 描述                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ 中止<br/>        | 0x80004004<br/> | 作業已中止，因為發生未指定的錯誤。<br/>                                                                              |
| E \_ ACCESSDENIED<br/> | 0x80070005<br/> | 一般拒絕存取的錯誤。<br/>                                                                                                          |
| E \_ 失敗<br/>         | 0x80004005<br/> | 發生未指定的失敗。<br/>                                                                                                    |
| E \_ 控制碼<br/>       | 0x80070006<br/> | 使用了不正確控制碼。<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | 一或多個引數無效。<br/>                                                                                                      |
| E \_ NOINTERFACE<br/>  | 0x80004002<br/> | [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))方法無法辨識要求的介面。 不支援此介面。<br/> |
| E \_ >NOTIMPL<br/>      | 0x80004001<br/> | 此方法尚未實作。<br/>                                                                                                          |
| E \_ OUTOFMEMORY<br/>  | 0x8007000E<br/> | 方法無法配置所需的記憶體。<br/>                                                                                         |
| E \_ 暫止<br/>      | 0x8000000A<br/> | 尚未提供完成作業所需的資料。<br/>                                                                      |
| E \_ 指標<br/>      | 且顯示0x80004003<br/> | 使用了不正確指標。<br/>                                                                                                            |
| E 未 \_ 預期<br/>   | 0x8000FFFF<br/> | 發生嚴重失敗。<br/>                                                                                                    |
| S \_ FALSE<br/>        | 0x00000001<br/> | 方法成功，並傳回布林值 **FALSE**。<br/>                                                                          |
| S \_ 確定<br/>           | 0x00000000<br/> | 此方法已成功。 如果預期會傳回布林值，則傳回值為 **TRUE**。<br/>                                            |



 

## <a name="network-errors"></a>網路錯誤

如果錯誤碼的前四個數字為8007，這表示系統或網路錯誤。 您可以使用 **net** 命令來解碼這些類型的錯誤。 若要解碼錯誤，請先將十六進位錯誤碼的最後四個數字轉換成 decimal。 然後，在命令提示字元中輸入下列命令，其中的十進位碼會以您要解碼的傳回值取代：

**net helpmsg <***十進位 \_ 碼***>**

Net 命令會傳回錯誤的描述。 例如，如果 COM 傳回錯誤8007054B，請將054B 轉換為 decimal (1355) 。 接著輸入下列內容：

**net helpmsg 1355**

Net 命令會傳回錯誤描述：「指定的網域不存在」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的錯誤處理](error-handling-in-com.md)
</dt> </dl>

 

 





