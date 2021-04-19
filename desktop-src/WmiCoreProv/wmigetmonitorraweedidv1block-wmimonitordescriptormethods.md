---
description: 取得指定的視頻電子產品標準關聯 () 增強的擴充顯示器識別資料 (E-EDID) 結構的原始資料，以定義設定監視的最佳設定。
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: WmiMonitorDescriptorMethods 類別的 WmiGetMonitorRawEEdidV1Block 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975435"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>WmiMonitorDescriptorMethods 類別的 WmiGetMonitorRawEEdidV1Block 方法

**WmiGetMonitorRawEEdidV1Block** 方法會取得指定的視頻電子產品標準關聯 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構，以定義監視設定的最佳設定。

## <a name="syntax"></a>語法


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*區塊識別碼* \[在\]
</dt> <dd>

資料區塊識別。

</dd> <dt>

*BlockType* \[擴展\]
</dt> <dd>

資料區塊的類型。 下表列出可能的傳回值。



| 值                                                                                 | 意義                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0) </dt> </dl>    | 未初始化：<br/>   |
| <dl> <dt>1 (0x1) </dt> </dl>    | EDID 基底區塊<br/> |
| <dl> <dt>2 (0x2) </dt> </dl>    | EDID 區塊對應<br/>  |
| <dl> <dt>255 (0xFF) </dt> </dl> | 其他<br/>           |



 

</dd> <dt>

*BlockContent* \[擴展\]
</dt> <dd>

128位元組陣列，其中包含原始區塊內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。

## <a name="examples"></a>範例

下列程式碼範例會將任何顯示的 EDID 區塊抓取為原始128位陣列。


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

