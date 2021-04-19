---
title: '預先定義的屬性 (Msctf .h) '
description: 下列值會識別 TSF 定義的屬性。 包含每個屬性類型的資料格式和內容。
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- 預先定義的屬性文字服務架構
topic_type:
- apiref
api_name:
- Predefined Properties
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807d1be5d1cc025971ad294fac825b89a4a0a519
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966138"
---
# <a name="predefined-properties"></a>預先定義的屬性

下列值會識別 TSF 定義的屬性。 包含每個屬性類型的資料格式和內容。

## <a name="properties"></a>屬性



| 屬性                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ \_ 屬性屬性**       | 包含 [**TfGuidAtom**](tfguidatom.md) 值，表示顯示內容的 **GUID** 。 [**ITfCategoryMgr：： GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) 是用來將此值轉換成 **GUID**。 如需詳細資訊，請參閱 [使用顯示內容](using-display-attributes.md)。                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ 的 \_ TEXTOWNER**       | 包含 [**TfGuidAtom**](tfguidatom.md) 值，表示擁有文字之文字服務 ( **CLSID** ) 的類別識別碼。 [**ITfCategoryMgr：： GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) 是用來將此值轉換成 **CLSID**。                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **GUID \_ 的 \_ LANGID**          | 包含 **DWORD** 值，其中包含低字組中文字 ( **LANGID** ) 的語言識別項。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **GUID \_ 的 \_ 讀取**         | 包含屬性所涵蓋之文字的語音閱讀文字。 這可能與實際文字不同。 Windows Store 應用程式不支援此屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_撰寫 GUID \_**       | 包含布林值，如果文字是組合的一部分則為非零值，否則為零。 如果這個屬性是 VT \_ 空白，則可以假設文字不是組合的一部分。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **GUID \_ 的 \_ MODEBIAS**        | 包含 [**TfGuidAtom**](tfguidatom.md) 值，表示支援的模式偏差類型。 [**ITfCategoryMgr：： GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) 是用來將此值轉換成 **GUID**。 這可以是其中一個 [**模式偏差值**](mode-bias-values.md)。                                                                                                                                                                                                                                                                                                                                                                                                  |
| **GUID \_ 的 \_ lifeATTICE 很愛**       | 包含 [**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice) 物件的指標。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **GUID \_ 的 \_ TKB \_ 替代項** | **從 Windows 8 開始：** 包含觸控鍵盤所設定的 **DWORD** 值。 TSF 感知的編輯控制項和應用程式可以使用這個屬性來識別屬性所涵蓋之文字範圍中文字的本質，例如，如果範圍中的文字是插入文字建議或自動校正的結果。 <br/> 屬性所涵蓋之文字範圍中的文字本質也會延伸至檔中該文字範圍之 [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) 介面所傳回的替代類型。<br/> 請參閱下列備註，以瞭解這個屬性的可能值。<br/> |



 

## <a name="remarks"></a>備註

**GUID 屬性 \_ \_ TKB \_ 替代** 屬性可以是下列其中一個值。



| Name                                     | 值      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TKB \_ 替換 \_ 標準                | 0x00000001 | 指出觸控鍵盤已針對屬性所涵蓋範圍中的文字產生可能的替代單字清單，且文字範圍和替代項都不是自動校正或文字建議。                                                                                                                                                                                                              |
| \_ \_ 適用于自動校正的 TKB 替代項 \_     | 0x00000002 | 指出觸控鍵盤已產生替代字，應自動取代屬性所涵蓋之文字範圍中的文字。<br/> 觸控鍵盤不會套用自動校正，而不會由編輯控制項或應用程式指示。 應該使用 ([**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) 的「重組」介面，將更正套用至檔中的文字。<br/> |
| \_ \_ 用於預測的 TKB 替代項 \_         | 0x00000003 | 指出屬性所涵蓋的文字範圍是由觸控鍵盤所產生並由使用者插入檔中的文字建議。<br/> 其他替代預測也可以儲存為檔中的屬性。<br/>                                                                                                                                                                     |
| 已套用 TKB \_ 替代 \_ 自動校正 \_ | 0x00000004 | 指出屬性所涵蓋的文字範圍是觸控鍵盤提供的自動校正，並透過 [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) 介面套用。<br/> 此值可供編輯控制項或應用程式使用，並具有 \_ \_ 適用于自動校正的 TKB 替代 \_ 項，以防止重複的自動校正應用程式。<br/>                                                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TfGuidAtom**](tfguidatom.md)
</dt> <dt>

[**ITfCategoryMgr：： GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[使用顯示內容](using-display-attributes.md)
</dt> <dt>

[**模式偏差值**](mode-bias-values.md)
</dt> <dt>

[**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





