---
title: 如何：使用設計工具變更 Windows Form DataGridView 資料行的類型
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], types
- DataGridView control [Windows Forms], changing column type
- data [Windows Forms], displaying
ms.assetid: 7f994d45-600d-4190-a187-35803214b40c
ms.openlocfilehash: 41ab0b36c5f3632ff4458d1289295ab2c9efe7c3
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855552"
---
# <a name="how-to-change-the-type-of-a-windows-forms-datagridview-column-using-the-designer"></a>如何：使用設計工具變更 Windows Form DataGridView 資料行的類型
有時候您會想要變更已新增至 Windows Forms 資料行的類型<xref:System.Windows.Forms.DataGridView>控制項。 比方說，您可能想要修改的某些資料行時將控制項繫結至資料來源自動產生的類型。 當您顯示的資料表有包含相關資料表中的資料列的外部索引鍵資料行時，這非常有用。 在此情況下，您可能要取代的文字 方塊中資料行顯示下拉式方塊資料行顯示更有意義的值，從相關資料表中的這些外部索引鍵。  
  
 下列程序需要**Windows 應用程式**表單，其中包含專案<xref:System.Windows.Forms.DataGridView>控制項。 如需這類專案的設定資訊，請參閱[如何： 建立 Windows 應用程式專案](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)並[如何： 將控制項加入 Windows Form](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)。  
  
> [!NOTE]
>  根據您目前使用的設定或版本，您所看到的對話方塊與功能表命令可能會與 [說明] 中描述的不同。 若要變更設定，請從 [ **工具** ] 功能表中選取 [ **匯入和匯出設定** ]。 如需詳細資訊，請參閱[將 Visual Studio IDE 個人化](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
### <a name="to-change-the-type-of-a-column-using-the-designer"></a>若要變更使用設計工具的資料行的類型  
  
1.  按一下智慧標籤圖像 (![智慧標籤圖像](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) 的右上角<xref:System.Windows.Forms.DataGridView>控制項，然後再選取**編輯資料行**。  
  
2.  選取的資料行**選取的資料行**清單。  
  
3.  在 **資料行屬性**方格中，設定`ColumnType`到新的資料行類型的屬性。  
  
    > [!NOTE]
    >  `ColumnType`屬性是只有設計階段屬性，指出代表資料行類型的類別。 它不是資料行類別中定義的實際屬性。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridViewColumn>  
 [如何： 建立 Windows 應用程式專案](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa)  
 [操作說明：將控制項新增至 Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)
