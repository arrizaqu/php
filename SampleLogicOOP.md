<?php

class SampleLogic{

    private $baris=0;
    private $kolom=0;
    private $data=array();

    public function setMatrix($input){
        $this->baris = $input;
        $this->kolom = $input;

        for ($i=0; $i < $this->baris; $i++) { 
            # code...
            for ($j=0; $j < $this->kolom; $j++) { 
                # code...
                if($i - $j == 0){
                    $this->data[$i][$j] = "$i.$j";
                } else {
                    $this->data[$i][$j] = "*";
                }
                
            } 
        }
    }

    public function showMatrix(){

        echo "<table>";
        for ($i=0; $i < $this->baris; $i++) { 
            # code...
            echo "<tr>";
            for ($j=0; $j < $this->kolom; $j++) { 
                # code...

                echo "<td>".@$this->data[$i][$j]."</td>";

            }
            echo "</tr>";
        }

        echo "</table>";
    }
}

$preview = new SampleLogic();
$preview->setMatrix(5);
$preview->showMatrix();
