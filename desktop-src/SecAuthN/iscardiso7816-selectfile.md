---
description: SelectFile 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會在邏輯通道內設定目前的基本檔。 後續命令可能會透過邏輯通道隱含地參考目前的檔案。
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816：： SelectFile 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192955"
---
# <a name="iscardiso7816selectfile-method"></a>ISCardISO7816：： SelectFile 方法

\[**SelectFile** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**SelectFile** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會在邏輯通道內設定目前的基本檔。 後續命令可能會透過邏輯通道隱含地參考目前的檔案。

在卡片檔案中選取 (DF) 的目錄（可能是檔案的根目錄 (MF) ）使其成為目前的 DF。 在這類選取專案之後，就可以透過該邏輯通道來參考隱含目前的基本檔。

選取基本檔案會將選取的檔案及其父系設定為目前的檔案。

在重設的答案之後，除非在歷程記錄的位元組或初始資料字串中指定不同，否則會透過基本邏輯通道隱含地選取 MF。

## <a name="syntax"></a>語法


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byP1* \[在\]
</dt> <dd>

選取控制項。



| P1 (word) 中的上層位元組： 8 7 6 5 4 3 2 1                                                                                                                                                            | 意義                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000xx**</dt><dt></dt> </dl> | 選取檔案識別碼<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF、DF 或 MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | 子 DF<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | DF 下的 EF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | 目前 DF 的父 DF<br/> |



 

當 P1 = 00 時，卡片知道檔案識別碼的特定編碼方式，或如果要選取的檔案是 MF、DF 或 EF，則知道命令的執行內容。

當 P1-P2 = 0000 時，如果已提供檔案識別碼，則在下列環境中應該是唯一的：

-   目前 DF 的直屬子系
-   父 DF
-   父 DF 的直屬子系

如果 P1-P2 = 0000，且資料欄位為空白或等於3F00，則選取 MF。

當 P1 = 04 時，資料欄位是 DF 名稱，可能會以正確的截斷。

在支援的情況下，後續具有相同資料欄位的這類命令，就應該選取名稱與資料欄位相符的 DFs (也就是從命令資料欄位) 開始。 如果卡片接受具有空白資料欄位的命令，則可以連續選取所有或 DFs 子集。

</dd> <dt>

*byP2* \[在\]
</dt> <dd>

選取控制項。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

需要作業的資料;否則 **為 Null**。 傳入此參數的資料類型包括：

-   檔案識別碼
-   來自 MF 的路徑
-   來自目前 DF 的路徑
-   DF 名稱

</dd> <dt>

*lBytesToRead* \[在\]
</dt> <dd>

空白 (，也就是 0) 或回應中預期的最大資料長度。

</dd> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。

傳回時，它會填入由這項作業所建立的 APDU 命令。 如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

除非另有指定，否則封裝命令的正確執行會根據下列規則來修改安全性狀態：

-   當目前的基本檔案變更，或沒有目前的基本檔案時，會遺失先前目前基本檔案的特定安全性狀態。
-   當目前的「可寫入的目錄」 (DF) 為的子系或與先前目前的 DF 相同時，就會遺失之前的目前 DF 的特定安全性狀態。 先前和新的目前 DF 的所有通用祖系通用的安全性狀態會維持不變。

如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
