---
description: 代表物件樹狀結構中建立為筆跡分析一部分的節點。
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: 'ICoNtextNode 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026251"
---
# <a name="icontextnode-interface"></a>ICoNtextNode 介面

代表物件樹狀結構中建立為筆跡分析一部分的節點。

## <a name="members"></a>成員

**ICoNtextNode** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ICoNtextNode** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ICoNtextNode** 介面具有這些方法。



| 方法                                                                                  | 描述                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddCoNtextLink**](icontextnode-addcontextlink.md)                                   | 將新的 [**ICoNtextLink**](icontextlink.md) 加入至 **ICoNtextNode** 物件的內容連結集合。<br/>                                                                                                          |
| [**AddPropertyData**](icontextnode-addpropertydata.md)                                 | 新增應用程式特定資料的片段。<br/>                                                                                                                                                                         |
| [**確認**](icontextnode-confirm.md)                                                 | 修改確認類型，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 物件可變更的 **ICoNtextNode** 內容。<br/>                                                                         |
| [**ContainsPropertyData**](icontextnode-containspropertydata.md)                       | 判斷 **ICoNtextNode** 物件是否包含儲存在指定之識別碼下的資料。<br/>                                                                                                                |
| [**CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md) | 建立子 **ICoNtextNode** 物件，其中只包含型別、識別碼和位置的資訊。<br/>                                                                                                          |
| [**CreateSubNode**](icontextnode-createsubnode.md)                                     | 建立新的子 **ICoNtextNode** 物件。<br/>                                                                                                                                                                       |
| [**DeleteCoNtextLink**](icontextnode-deletecontextlink.md)                             | 從 **ICoNtextNode** 物件的連結集合中刪除 [**ICoNtextLink**](icontextlink.md)物件。<br/>                                                                                                         |
| [**DeleteSubNode**](icontextnode-deletesubnode.md)                                     | 移除子 **ICoNtextNode**。<br/>                                                                                                                                                                                  |
| [**GetCoNtextLinks**](icontextnode-getcontextlinks.md)                                 | 抓取 [**ICoNtextLink**](icontextlink.md) 物件的集合，這些物件表示與其他 **ICoNtextNode** 物件的關聯性。<br/>                                                                          |
| [**GetId**](icontextnode-getid.md)                                                     | 捕獲 **ICoNtextNode** 物件的識別碼。<br/>                                                                                                                                                          |
| [**GetLocation**](icontextnode-getlocation.md)                                         | 抓取 **ICoNtextNode** 物件的位置和大小。<br/>                                                                                                                                                    |
| [**GetParentNode**](icontextnode-getparentnode.md)                                     | 在內容節點樹狀結構中，捕獲此 **ICoNtextNode** 的父節點。<br/>                                                                                                                                       |
| [**GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)                     | 抓取值，這個值會指出 **ICoNtextNode** 物件是否已部分擴展或完整填入。<br/>                                                                                                   |
| [**GetPropertyData**](icontextnode-getpropertydata.md)                                 | 取得指定之識別碼的應用程式特定資料或其他屬性資料。<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | 抓取具有屬性資料的識別碼。<br/>                                                                                                                                                        |
| [**GetStrokeCount**](icontextnode-getstrokecount.md)                                   | 捕獲與 **ICoNtextNode** 物件相關聯的筆劃數目。<br/>                                                                                                                                       |
| [**GetStrokeId**](icontextnode-getstrokeid.md)                                         | 抓取 **ICoNtextNode** 物件內索引值所參考之筆劃的筆觸識別碼。<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | 抓取 **ICoNtextNode** 物件內筆劃的識別碼陣列。<br/>                                                                                                                              |
| [**GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)                 | 取得陣列，其中包含指定之筆劃的封包屬性資料。<br/>                                                                                                                                   |
| [**GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)   | 取得陣列，其中包含指定之筆劃的封包屬性識別碼。<br/>                                                                                                                            |
| [**GetSubNodes**](icontextnode-getsubnodes.md)                                         | 抓取 **ICoNtextNode** 物件的直接子節點。<br/>                                                                                                                                                   |
| [**GetType**](icontextnode-gettype.md)                                                 | 捕獲 **ICoNtextNode** 物件的型別。<br/>                                                                                                                                                                 |
| [**GetTypeName**](icontextnode-gettypename.md)                                         | 抓取這個 **ICoNtextNode** 的人們看得懂的型別名稱。<br/>                                                                                                                                                     |
| [**IsConfirmed**](icontextnode-isconfirmed.md)                                         | 抓取指出是否已確認 **ICoNtextNode** 物件的值。 [**IInkAnalyzer**](iinkanalyzer.md) 無法變更已確認 **ICoNtextNode** 物件的節點類型和相關聯的筆劃。<br/> |
| [**LoadPropertiesData**](icontextnode-loadpropertiesdata.md)                           | 針對先前使用 [**ICoNtextNode：： SavePropertiesData**](icontextnode-savepropertiesdata.md)建立的位元組陣列，重新建立應用程式特定和內部屬性資料。<br/>                  |
| [**MoveSubNodeToPosition**](icontextnode-movesubnodetoposition.md)                     | 將指定的子 **ICoNtextNode** 物件重新排序為指定的索引。<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | 移除應用程式特定的資料片段。<br/>                                                                                                                                                                      |
| [**父**](icontextnode-reparent.md)                                               | 將這個 **ICoNtextNode** 物件從其父內容節點的子節點集合移至指定的內容節點的子節點集合。<br/>                                                                         |
| [**ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)               | 將筆劃資料從此 **ICoNtextNode** 移動到指定的 **ICoNtextNode**。<br/>                                                                                                                                    |
| [**SavePropertiesData**](icontextnode-savepropertiesdata.md)                           | 抓取位元組陣列，其中包含此 **ICoNtextNode** 的應用程式特定和內部屬性資料。<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | 更新此 **ICoNtextNode** 的位置和大小。<br/>                                                                                                                                                            |
| [**SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)                     | 修改指出此 **ICoNtextNode** 為部分或完整擴展的值。<br/>                                                                                                                   |
| [**SetStrokes**](icontextnode-setstrokes.md)                                           | 將指定的筆觸與這個 **ICoNtextNode** 相關聯。<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>備註

節點的類型在 [內容節點類型](context-node-types.md) 常數中有描述。

## <a name="examples"></a>範例

下列範例顯示檢查 **ICoNtextNode** 的方法;方法會執行下列動作：

-   取得內容節點的型別。 如果內容節點是未分類的筆墨、分析提示或自訂辨識器節點，則會呼叫 helper 方法來檢查節點類型的特定屬性。
-   如果節點有子節點，它會藉由呼叫本身來檢查每個子節點。
-   如果節點是筆墨分葉節點，它會藉由呼叫 helper 方法來檢查節點的筆劃資料。

下列 InkAnalysis API 可讓您建立包含筆墨單字和文字單字的行節點。 不過，剖析器會忽略這些混合節點，並將它們視為外部節點。 這會影響使用者在此混合節點上或周圍書寫時偵測筆墨注釋的剖析精確度。


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNodes**](icontextnodes.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

